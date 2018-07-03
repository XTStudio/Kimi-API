# UIKit | Interfaces

```typescript

/**
 * A structure that contains the location and dimensions of a rectangle.
 */
Rect = {x: number, y: number, width: number, height: number}

/**
 * A structure that contains a point in a two-dimensional coordinate system.
 */
Point = {x: number, y: number}

/**
 * A structure that contains width and height values.
 */
Size = {width: number, height: number}

/**
 * An affine transformation matrix for use in drawing 2D graphics.
 * @see https://developer.apple.com/documentation/coregraphics/cgaffinetransform?language=objc
 */
AffineTransform = {a: number, b: number, c: number, d: number, tx: number, ty: number}

/**
 * The inset distances for views.
 */
EdgeInsets = {top: number, left: number, bottom: number, right: number}

/**
 * A structure used to describe a portion of a series, such as characters in a string or objects in an array.
 */
Range = {location: number, length: number}

```