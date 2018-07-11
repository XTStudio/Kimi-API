# CoreGraphics | CAGradientLayer extends CALayer

A layer that draws a color gradient over its background color, filling the shape of the layer (including rounded corners)

```typescript

/**
 * An array of UIColor objects defining the color of each gradient stop.
 */
colors: UIColor[]

/**
 * An optional array of NSNumber objects defining the location of each gradient stop. 
 */
locations: number[]

/**
 * The start point of the gradient when drawn in the layer’s coordinate space.
 */
startPoint: Point

/**
 * The end point of the gradient when drawn in the layer’s coordinate space.
 */
endPoint: Point

```