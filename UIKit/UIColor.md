# UIKit | UIColor

An object that stores color data and sometimes opacity (alpha value).

```typescript
/**
 * Preset colors
 */
static blackColor: UIColor
static clearColor: UIColor
static grayColor: UIColor
static redColor: UIColor
static yellowColor: UIColor
static greenColor: UIColor
static blueColor: UIColor
static whiteColor: UIColor

/**
 * Creates and returns a color object using the specified opacity and RGB component values. 
 */
constructor(r: number, g: number, b: number, a: number): UIColor
```