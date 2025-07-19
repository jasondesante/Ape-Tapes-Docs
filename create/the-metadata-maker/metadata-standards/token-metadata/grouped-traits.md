# Grouped Traits

These grouped traits are all found in the Extras tab in the song metadata maker.

### Attributes

Attributes are the traits that show up when you view an NFT on a marketplace site like OpenSea, Magic Eden, Blur, etc. Those traits that show up are the attributes. It's an important section that every NFT needs if they want the traits to show up on secondary marketplaces the same way attributes show up for all other NFTs.

### Credits

Credits is an array of traits that describe the individual credits for the token.  In here you can be as detailed as you want. This is the spot where you can list every person involved in the creation.

### Stems

Stems are a form of multi track, where each "stem" is an individual or group of tracks. When you combine the stems it forms the song.  Providing stems unlocks remixing potential, and stem player potential.  This is an important option to have in a music nft metadata standard.

### Mixes

Alternate mixes are a powerful feature that lets you include unlimited variations of your track, each with programmable conditions that trigger different listening experiences.&#x20;

Think instrumental, acapella, demos, variations of the solo, bridge or outro. Endless ways to enhance.

Think Nintendo's dynamic arrangements in Mario or Animal Crossing, now possible with music NFTs. You can be as wild or subtle as you want, programming experiences previously only found in video games while imagining entirely new possibilities that have never existed before. This is a very serious, important feature. This is why we're here.

Some example conditions that have been built into [The Metadata Maker](../../) are:

* Weight - set the number to weigh the mix's chance of being chosen when randomized.  For example if there are 3 mixes, with weights 1, 2, and 3. That adds up to 6 points across 3 mixes. The mix with weight 3 will occupy 3/6 total chances of being picked.  The mix with weight 1 will have a 1/6 chance.  The mix with weight 2 will have a 1/3 chance of being picked.  The mix with weight 3 will have a 1/2 chance of being picked.  Because the weights are all added up, and that's how you get your probability.
* Weather - set the weather to be able to play the mix
* Day - set the day of the week to be able to play the mix
* Start Time - set the start time of day to be able to play the mix.  Before the start time the mix is unplayable, starting at midnight, unless an End Time is also set.
* End Time - set the end time of day to be able to play the mix.  After the end time the mix is unplayable until the next day.  Resets at midnight unless a Start Time is also set.
* Minimum Plays - set the min number of plays to be on a song for this mix to be playable (can be 0 or higher).  This makes the mix unlocked after a certain amount of logged plays.
* Maximum Plays - set the max number of plays to be on a song for this mix to be playable (can be 1 or higher).  This makes the mix unplayable after a certain amount of logged plays.
* Every x Plays - set how many plays in between this mix having another chance to be played (can only be 2 or higher).  Once it's been played you have to wait a certain amount of logged plays until it's weights affect the mix choice.
* Altitude - will play at a certain altitude
* Favorite - will play if you favorite the song
* Birthday - will play on your birthday
