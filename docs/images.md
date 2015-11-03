# Pointslocal Images

> Images in the Pointslocal system can be referenced by context (event, venue, team, story, etc) and cropped in a myriad ways.  All image references will begin with ```http://[yoursite]/image?method=icrop&context=[context]&w=?&h=?```

##### Request Parameters
- **w** ```int``` - Width of desired, cropped image.  Can be set to -1 to scale proportionally given a fixed height.
- **h** ```int``` - Height of desired, cropped image.  Can be set to -1 to scale proportionally given a fixed width.
- **context** ```enum``` - A context for the image type.  General detail on each context type can be found within respective API pages.
- **cropmode** ```enum``` - A style of crop to return.  ```topbias``` will yield to the top of the image, ```botbias``` will yield to the bottom and ```featbias``` will attempt to detect features and bias to capture that centroid.  If ```featbias``` fails, the crop mode will revert to the x/y center of the image.
- **effect** ```enum``` - Applies a visual effect to the image.  Currently supports "darkgradient" which applies a midpoint to bottom of image darkening gradient over the image.
- **trim** ```int``` - If set to 1, will attempt to automatically remove stray whitespace around an image.
