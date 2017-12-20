# Rundown

RhythmHQ is an independent radio station built using Flask and Zappa. It's deployed as a "serverless" app with AWS Lambda. 

# How it works

RhythmHQ works by reading an IceCast server page (using ajax). If it can't find the page, an "offline" modal is displayed to the user. Track titles are found by reading an IceCast status-json.xsl file which contains the currently playing track's title. If the track title is found, it puts the track title into a SoundCloud search query. All artists played by the station are shown by clicking the logo at the top of the page, which displays a modal box listing them in alphabetical order. Modal boxes on the site are managed using [Sweetalert 2](https://limonte.github.io/sweetalert2/) All of the code can be found in the [pops.js file](https://github.com/kyoto-shift/rhythmhq-flask/blob/master/static/scripts/pops.js).
