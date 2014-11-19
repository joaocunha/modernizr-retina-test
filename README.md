Modernizr Retina Test
=====================

A simple and quick Modernizr test for retina / high resolution / high pixel density. Should run in less than half a milisecond.

It's worth mentioning that there is no consensus on what can be considered "high resolution" - some devices offer 1.3dpr, some 1.5dpr, some 2dpr, etc. For the sake of making things easier, we are considering any pixel density ratio above 1 as high resolution.

```js
/**
 * Modernizr test for retina / high resolution / high pixel density
 *
 * @author Joao Cunha
 * @license MIT
 */
 
Modernizr.addTest('hires', function() {
    // starts with default value for modern browsers
    var dpr = window.devicePixelRatio ||
 
    // fallback for IE
        (window.screen.deviceXDPI / window.screen.logicalXDPI) ||
 
    // default value
        1;
 
    return !!(dpr > 1);
});
```
