# UIKit | UIColor

An object that stores color data and sometimes opacity (alpha value).

```typescript
/**
 * Preset colors
 */
static readonly blackColor: UIColor
static readonly clearColor: UIColor
static readonly grayColor: UIColor
static readonly redColor: UIColor
static readonly yellowColor: UIColor
static readonly greenColor: UIColor
static readonly blueColor: UIColor
static readonly whiteColor: UIColor

/**
 * Creates and returns a color object using the specified opacity and RGB component values. 
 */
constructor(r: number, g: number, b: number, a: number): UIColor
```