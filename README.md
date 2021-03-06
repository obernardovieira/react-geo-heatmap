# react-geo-heatmap
Inspired by [geo-heatmap](https://github.com/luka1199/geo-heatmap), a very simple next.js / react app that creates an interactive geo heatmap from your Google location history.   
This app uses :  
[next.js](https://github.com/zeit/next.js)  
[react-leaflet](https://github.com/PaulLeCam/react-leaflet)  
[react-leaflet-heatmap-layer](https://github.com/OpenGov/react-leaflet-heatmap-layer)  
[supercluster](https://github.com/mapbox/supercluster#readme)  to manage such large files and prevent map to lag.

![cattura3](https://user-images.githubusercontent.com/8511928/71216840-00bffe80-22bc-11ea-9548-6cbe72f17288.gif)

## Getting Started
### Get your location data
You can download  your location data here: https://takeout.google.com/  
You only need to select, and download, "Location History", choose Json as file format.  

### Installation
If not done yet install [ Node.js](https://nodejs.org/) and npm.  
Next clone this repository,rename your location history to `history.json` and  move it to  `public/history.json`.   
From a command shell run `npm install` to install dependencies, then `npm run dev`  for development mode or  follow next.js [instructions](https://nextjs.org/learn/basics/deploying-a-nextjs-app) for building the app for production.

### Usage
Running `npm run dev` will open your browser on `http://localhost:3000/` 
You can now filter and update the  heatmap of your location history by date or activity type.  
You can also change heatmap supercluster settings, full reference of options can be found [here](https://github.com/mapbox/supercluster#options).

### Testing
You can test the app with random geo-data, run `node randomData.js` by default it  generate 1000000 points (~200MB) , you can override this number passing `count` as argoument ex. `node randomData.js --count=1000`.  
Note that this command will overwrite any existing `history.json` file.
