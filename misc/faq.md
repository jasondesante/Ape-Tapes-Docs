# FAQ

## I am seeing a warning when logging in with Metamask

This is because of the site being hosted on Arweave, and Metamask wanting the server and front end to have matching urls.  This is normal and can be solved by using the specific arns and gateway "contractwizard.arweave.net".

The server is telling the wallet the site is "contractwizard.arweave.net" and any other gateway/arns will show the warning. If the server told metamask the site was "ar://listen" then it would still show warnings. So currently if you go to "listen.ar.io", for example, you will see a warning in your Metamask wallet that is telling you that the server and the website are not matching.  This is normal. Hopefully in the future Metamask will have a cool solution for sites that are hosted with Arweave that use ARNS.

You can currently access the site through the arns "listen" and "contractwizard". Both ar://listen and ar://contractwizard work. Going forward I think "listen" should be the main arns, and maybe I use the "contractwizard" arns for a direct link to just the creation tools.  I'm open to your suggestions.





## Why are none of the pictures loading?

Use a VPN!  Your ISP must be blocking Arweave. &#x20;

This is a common issue if you live in Australia and similar countries.
