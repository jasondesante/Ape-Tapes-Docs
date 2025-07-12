# Playlist Tags

## Custom Tags

Uploaded playlists have Contract Wizard playlist tags on Arweave to let anyone search all published playlists with these tags with a simple query using GraphQL. &#x20;

Right now there are 4 playlist tags being used.  The playlists are currently being tagged with:

* Playlist: Contract-Wizard
* Playlist-Version: 0.2
* Playlist-Creator
* Playlist-Name

Setting the "Playlist" tag to "Contract-Wizard" is meant to signify that the type of playlist is from The Contract Wizard.

Setting the "Playlist-Version" tag to "0.2" is the version of the metadata. It used to be 0.1 but then I changed something.

The "Playlist-Creator" tag is the address of the creator of the playlist

The "Playlist-Name" tag is the name of the playlist

[Here](https://viewblock.io/arweave/tx/26kAioACfUPgri8iHxPf7d2zoWepwFies9Gw8rarCRM) is an example of a published playlist.

### Query Playlist Data

You can do a query and see what happens when you search Playlist: Contract-Wizard.

What happens if you search Playlist-Creator and add a wallet?

{% embed url="https://arweave-search.goldsky.com/graphql" %}
