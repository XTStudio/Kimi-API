# UIKit | UIColor

An object that stores color data and sometimes opacity (alpha value).

```typescript
/**
 * Preset colors
 */
static readonly black: UIColor
static readonly clear: UIColor
static readonly gray: UIColor
static readonly red: UIColor
static readonly yellow: UIColor
static readonly green: UIColor
static readonly blue: UIColor
static readonly white: UIColor

/**
 * Returns a color object using the specified opacity and RGB / ARGB hex values. 
 * eg: #ffffff means white color.
 * eg: #ffff0000 means red color with 1.0 alpha.
 */
static hexColor(hexValue: string): UIColor

/**
 * Creates and returns a color object using the specified opacity and RGB component values. 
 */
constructor(r: number, g: number, b: number, a: number): UIColor
```