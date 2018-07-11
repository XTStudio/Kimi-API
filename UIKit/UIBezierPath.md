# UIKit | UIBezierPath

A path that consists of straight and curved line segments that you can render in your custom views.

```typescript

/**
 * Moves the receiver’s current point to the specified location.
 */
moveTo(toPoint: Point): void

/**
 * Appends a straight line to the receiver’s path.
 */
addLineTo(toPoint: Point): void

/**
 * Appends an arc to the receiver’s path.
 */
addArcTo(toCenter: Point, radius: number, startAngle: number, endAngle: number, closewise: boolean): void

/**
 * Appends a cubic Bézier curve to the receiver’s path.
 */
addCurveTo(toPoint: Point, controlPoint1: Point, controlPoint2: Point): void

/**
 * Appends a quadratic Bézier curve to the receiver’s path.
 */
addQuadCurveTo(toPoint: Point, controlPoint: Point): void

/**
 * Closes the most recently added subpath.
 */
closePath(): void

/**
 * Removes all points from the receiver, effectively deleting all subpaths.
 */
removeAllPoints(): void

/**
 * Appends the contents of the specified path object to the receiver’s path.
 */
appendPath(path: UIBezierPath): void

```