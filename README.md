# Rundown

RhythmHQ is an independent radio station built using [Flask](http://flask.pocoo.org/) and deployed using [Zappa](https://github.com/Miserlou/Zappa). It's essentially a "serverless" app.

# How it works

RhythmHQ works by reading an IceCast server page *(using ajax)*. If it can't find the page, an "offline" modal is displayed to the user.
If the server page is found and the stream is online, a heavily modified [Ableplayer](https://ableplayer.github.io/ableplayer/) plays the audio.

Track titles are found by reading an IceCast status-json.xsl file *(using ajax)* which contains the current playing track's title. If the track title is found, it's then put into a SoundCloud search query, then finally passed to the "Now Playing" link under the player. Clicking the logo displays a modal box listing all of the artists played by the station in alphabetical order. Modal boxes on the site are managed using [Sweetalert 2](https://limonte.github.io/sweetalert2/).

All of the code can be found in the [pops.js](https://github.com/kyoto-shift/rhythmhq-flask/blob/master/static/scripts/pops.js) file.
