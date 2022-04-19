# draw2d-wrapper
draw2d-eb-wrapper including missing features like "semanticPorts"

#### In this repository you will find a draw2d-wrapper. The wrapper is based on the draw2d-eb-wrapper, which is available as an npm package.
#### The first thing added is the logic of the "semanticPorts".
#### If more features of the existing draw2d-project are missing in the wrapper, feel free to contact me. I will be happy to add missing features.

### Angular
To add the wrapper to an existing Angular project, you need to do the following:

1. Copy this js-file to Copy the js file into one of the folders of the Angular project
2. Add the path to the draw2d-wrapper.js under scripts in angular.json
3. Add the Code to {name}.component.ts
```
declare var draw2d: any;
```
4. Use the files from the draw2d project to create your own project.

E.g. (in BoundingboxFigure.js): 
```let BoundingboxFigure = draw2d.shape.basic.Rectangle.extend({.....});```

E.g. (in {name}.component.ts):  
```declare let BoundingboxFigure: any;```   
```...```   
```let canvas = new draw2d.Canvas("gfx_holder");```     
```canvas.add(new BoundingboxFigure({id:"42", x:100, y:100}));```

5. Add the path to the BoundingBoxFigure.js under scripts in angular.json
