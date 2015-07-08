# Temperature Map
Library to draw temperature maps (heat maps) using Canvas/Javascript. Drawing shows an animation and does not block the main process.

### Run

Download this project with:

git clone https://github.com/optimisme/javascript-temperatureMap.git

cd javascript-temperatureMap

Open the example file with a web navigator:

index.html

temperatureMap.js contains the libary source

### Using the library

can0 = document.getElementById("cns0"); // Get the canvas object
ctx0 = can0.getContext("2d");           // Get the canvas context
drw0 = new TemperatureMap(ctx0);        // Create the object 

drw0.setRandomPoints(25, width, height);// Assign rando points
                                        // Or assign points with drw0.setPoints(arr, width, height
                                       
// To draw the fast map
drw0.drawLow(function () {              // Draw 'low' resolution image
    drw0.drawPoints();                  // Draw points information when done
});

// To draw the full map with levels
drw1.drawFull(false, function () { /* Do nothing when done */ });


### Example 0

Animation showing a random temperature map with:

- Low resolution (fast map)

![eg0](https://raw.github.com/optimisme/javascript-temperatureMap/master/captures/eg0.png)

### Example 1

Animation showing a temperature map using previous points:

- Full resolution (slow map)
- Colors by gradients

![eg1](https://raw.github.com/optimisme/javascript-temperatureMap/master/captures/eg1.png)

### Example 2

Animation showing a temperature map using previous points:

- Full resolution (slow map)
- Colors by levels

![eg2](https://raw.github.com/optimisme/javascript-temperatureMap/master/captures/eg2.png)
