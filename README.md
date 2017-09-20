![Lighthouse Octopus Pun](https://en.1jux.net/scale_images/218118_b.jpg "Lighthouse Octopus Pun")

[Lighthouse](https://github.com/GoogleChrome/lighthouse) changing the color
of [Philips Hue](https://www.developers.meethue.com/philips-hue-api) light bulbs
based on overall report score.

### Get started

    npm install

If you've already installed the app and just want to pull the latest deps:

   npm upgrade

### Run it

#### Kiosk mode

To run "kiosk mode", use:

    npm run kiosk

This will start a webserver and open two browser windows to the app. One is a
kiosk UI (http://localhost:8080?kiosk) that you should drag to a larger monitor
and the other is where users input a URL to test Lighthouse (http://localhost:8080).

#### Standalone mode

To only start a webserver, use:

    npm start

#### Running stable Chrome

To run a different version of Chrome (e.g. Stable), specify the `CHROME_PATH` env variable:

```
CHROME_PATH="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" npm start
CHROME_PATH="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" npm kiosk
```

### Setup it

Create a `.hueusername` in the root folder and fill it with a username
registered on your Hue Bridge. If you don't have a username:

1. press the Link Button on the Hue Bridge
2. run the app (below). Doing so will create a "Lighthouse" user on the bridge.

```
node index.js <URL>
node index.js --view <URL>
node index.js --output=json --output-path=results.json <URL>
```

This should launch Chrome and run Lighthouse against the URL that you input.
