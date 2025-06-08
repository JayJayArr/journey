# Spotify Part

After creating an API the next project I went after was a personal wish:
Controlling Spotify Music queues on a massive scale.
At a party many different people have music wishes and it is not always possible to handle all the wishes.
The simple solution is a voting system.
Let people suggest songs.
Let all of the other guests vote on them and push the most liked song into the currently playing queue.
The host still chooses a playlist and has the full control.
But every x minutest the most liked song from the community gets played.

The first time I tried to build this it ended up being a nest.js and angular application.
At the end it **kinda** worked. You could search for songs, suggest them, vote for them and at the end they were actually played.
But of course it was far from perfect.
I had no idea what a websocket is and far too many requests were just forwarded to the spotify API.
Angular services? Aint nobody got time for that.
And no tests anywhere.
I ran it on some personal parties, it worked fine, everyone had to be connected to the same WIFI but it was fine.

At the end this App was the first one that would fall to the "rewrite it in Rust" meme.
