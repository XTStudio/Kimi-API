# CoreGraphics | CAShapeLayer extends CALayer

A layer that draws a cubic Bezier spline in its coordinate space.

```typescript

/**
 * The path defining the shape to be rendered.
 */
path: UIBezierPath | undefined

/**
 * The color used to fill the shape’s path.
 */
fillColor: UIColor | undefined

/**
 * The fill rule used when filling the shape’s path.
 */
fillRule: CAShapeFillRule

/**
 * Specifies the line cap style for the shape’s path.
 */
lineCap: CAShapeLineCap

/**
 * The dash pattern applied to the shape’s path when stroked.
 */
lineDashPattern: number[]

/**
 * The dash phase applied to the shape’s path when stroked.
 */
lineDashPhase: number

/**
 * Specifies the line join style for the shape’s path.
 */
lineJoin: CAShapeLineJoin

/**
 * Specifies the line width of the shape’s path.
 */
lineWidth: number

/**
 * The miter limit used when stroking the shape’s path.
 */
miterLimit: number

/**
 * The color used to stroke the shape’s path.
 */
strokeColor: UIColor | undefined

/**
 * The relative location at which to begin stroking the path.
 */
strokeStart: number

/**
 * The relative location at which to stop stroking the path.
 */
strokeEnd: number

```

## CAShapeFillRule

```typescript

enum CAShapeFillRule {
    nonZero,
    evenOdd,
}

```

## CAShapeLineCap

```typescript

enum CAShapeLineCap {
    butt,
    round,
    square,
}

```

## CAShapeLineJoin

```typescript

enum CAShapeLineJoin {
    miter,
    round,
    bevel,
}

```