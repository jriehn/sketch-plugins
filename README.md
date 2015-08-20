# sketch-plugins

var doc = context.document
var currentZoom = doc.zoomValue() * 100; // e.g., 0.8 = 80% zoom

zoom = doc.askForUserInput_initialValue("Enter custom zoom value", currentZoom.toString());
zoom = zoom.replace(/[^\d.-]/g, ''); // removes non-numeric, retains floats

doc.setZoomValue(zoom * .01);
