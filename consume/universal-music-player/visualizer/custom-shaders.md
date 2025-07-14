# Custom Shaders

A cool feature of the visualizer is the ability to bring your own custom written shaders and import them into the shader layer. Just open the shader menu and click "Create New" to code a custom shader.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-13 at 11.50.18 PM.png" alt=""><figcaption><p>Add your own custom shaders with the "Create New" button</p></figcaption></figure>

## Audio-Reactive Fragment Shaders

The visualizer uses **fragment shaders** - specialized programs that run on your GPU to generate real-time graphics. These shaders execute once for every pixel on your screen, potentially millions of times per frame, which is why they can create such smooth and complex visual effects.

### How It Works

Fragment shaders are written in **GLSL** (OpenGL Shading Language), a C-like programming language designed specifically for graphics programming. Each shader receives information about the current pixel being processed (like its screen coordinates) along with global data like timing and audio information. The shader then calculates what color that specific pixel should be based on mathematical formulas, noise functions, and the incoming audio data.

What makes these shaders special for music visualization is their ability to sample audio frequency data in real-time. The audio is processed into a texture containing 128 frequency bands from bass to treble, allowing the visual effects to react dynamically to different parts of the music spectrum.

### Available Variables

When writing custom shaders, you have access to these built-in variables:

* `uniform float time` - Animation time in seconds
* `uniform vec2 resolution` - Viewport size in pixels
* `uniform float audioLevel` - Overall audio level (0.0-1.0)
* `uniform sampler2D audioTexture` - Audio frequency data (128x1 texture)

To sample audio data, use: `texture2D(audioTexture, vec2(frequency, 0.0)).r` where frequency ranges from 0.0 (bass) to 1.0 (treble).

### Essential Techniques & Tips

**Coordinate Setup** Most shaders start by normalizing coordinates to a -1 to 1 range centered on screen:

glsl

```glsl
vec2 uv = (gl_FragCoord.xy - 0.5 * resolution.xy) / min(resolution.x, resolution.y);
```

This gives you a coordinate system that works consistently across different screen sizes.

### **Audio Sampling Strategies**

* **Bass frequencies**: Sample around `0.05-0.15` for kick drums and deep bass
* **Mid frequencies**: Sample around `0.3-0.6` for vocals and melody
* **Treble frequencies**: Sample around `0.8-0.95` for cymbals and bright sounds
* **Smooth multiple samples** for more stable readings: average several nearby frequency bins
* **Apply `pow()` functions** like `pow(audioSample, 0.7)` to make audio response feel more natural

### **Color Generation**

glsl

```glsl
// HSV-style color cycling
vec3 vibrantColor(float t) {
    return 0.5 + 0.5 * cos(6.28 * (t + vec3(0.0, 0.33, 0.67)));
}
```

This creates smooth color transitions perfect for audio-reactive effects.

**Shape Creation** Use `smoothstep()` for crisp, anti-aliased edges:

glsl

```glsl
float circle = smoothstep(0.1, 0.05, length(uv) - radius);
```

### **Animation Patterns**

* Combine `sin()` and `cos()` with time for organic movement
* Use `fract()` to create repeating patterns
* Modulate time with audio: `time * (1.0 + bassLevel * 0.5)` for tempo-reactive speed

### **Performance Tips**

* Minimize texture lookups - sample audio once and reuse values
* Use `const` for loop limits when possible
* Prefer mathematical functions over complex branching
* Keep loop counts reasonable (under 20-30 iterations)

### Creative Possibilities

Fragment shaders can create virtually any visual effect imaginable - from simple geometric patterns to complex fractal landscapes, particle systems, and psychedelic distortions. The examples show techniques like kaleidoscope symmetry, particle trails, frequency-based color mapping, and morphing blob shapes. Since they run entirely on the GPU, they can handle incredible complexity while maintaining smooth 60fps performance, making them perfect for responsive music visualization.
