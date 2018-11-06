# Canned Apps

A skeleton project which can be run and used to create a portable "copy" of a website. A "canned app" is just a snapshot of an HTML application, together with the API data that is required to run it, such that running it locally requires no external API calls. 

You will often need to open up the "canned-app-data" folder, navigate to a file, and manually tweak it. An example is a guide application that uses `var start = Date.now()` and then calls an API with that value. You would likely need to find the main JavaScript file and hardcode `Date.now = function(){return 1541526334919;};` so that it doesn't kepp calling the API with a unique date, as that would never be the same when re-running the canned applicaiton.

## Installation

```bash
npm install
```

## Use:

### `npm run server`

Assuming your app URL is 'https://www.yahoo.com/' you would then visit:

`http://localhost:8092/yahoo-stuff/https/www.yahoo.com/`

That would load that URL, and replace each path in the document with a locally routed URL, for example:
 
 - Before `https://someUrl/someImage.png` 
 - After: `http://localhost:8092/yahoo-stuff/https/someUrl/someImage.png`
 
 
For each application you capture, it is recommended that you utilize a unique string, in the above example we used 'yahoo-stuff'. All content would then be:

```bash
ls ./canned-app-data/yahoo-stuff
      

```
