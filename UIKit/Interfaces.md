# UIKit | Interfaces

```typescript

/**
 * A structure that contains the location and dimensions of a rectangle.
 */
UIRect = {x: number, y: number, width: number, height: number}

/* The "zero" rectangle -- equivalent to UIRectMake(0, 0, 0, 0). */
UIRectZero: UIRect

/**
 * Make a rect from `(x, y; width, height)'.
 */
UIRectMake(x: number, y: number, width: number, height: number): UIRect

/* Return true if `rect1' and `rect2' are the same, false otherwise. */
UIRectEqualToRect(rect1: UIRect, rect2: UIRect): boolean

/* Inset `rect' by `(dx, dy)' -- i.e., offset its origin by `(dx, dy)', and
   decrease its size by `(2*dx, 2*dy)'. */
UIRectInset(rect: UIRect, dx: number, dy: number): UIRect

/* Offset `rect' by `(dx, dy)'. */
UIRectOffset(rect: UIRect, dx: number, dy: number): UIRect

/* Return true if `point' is contained in `rect', false otherwise. */
UIRectContainsPoint(rect: UIRect, point: UIPoint): boolean

/* Return true if `rect2' is contained in `rect1', false otherwise. `rect2'
   is contained in `rect1' if the union of `rect1' and `rect2' is equal to
   `rect1'. */
UIRectContainsRect(rect1: UIRect, rect2: UIRect): boolean

/* Return true if `rect1' intersects `rect2', false otherwise. `rect1'
   intersects `rect2' if the intersection of `rect1' and `rect2' is not the
   null rect. */
UIRectIntersectsRect(rect1: UIRect, rect2: UIRect): boolean

/**
 * A structure that contains a point in a two-dimensional coordinate system.
 */
UIPoint = {x: number, y: number}

/* The "zero" point -- equivalent to UIPointMake(0, 0). */
UIPointZero: UIPoint

/**
 * Make a point from `(x, y)'.
 */
UIPointMake(x: number, y: number): UIPoint

/* Return true if `point1' and `point2' are the same, false otherwise. */
UIPointEqualToPoint(point1: UIPoint, point2: UIPoint): boolean

/**
 * A structure that contains width and height values.
 */
UISize = {width: number, height: number}

/* The "zero" size -- equivalent to UISizeMake(0, 0). */
UISizeZero: UISize

/**
 * Make a size from `(width, height)'.
 */
UISizeMake(width: number, height: number): UISize

/* Return true if `size1' and `size2' are the same, false otherwise. */
UISizeEqualToSize(size1: UISize, size2: UISize): boolean

/**
 * An affine transformation matrix for use in drawing 2D graphics.
 * @see https://developer.apple.com/documentation/coregraphics/cgaffinetransform?language=objc
 */
UIAffineTransform = {a: number, b: number, c: number, d: number, tx: number, ty: number}

/* The identity transform: [ 1 0 0 1 0 0 ]. */
UIAffineTransformIdentity: UIAffineTransform

/* Return the transform [ a b c d tx ty ]. */
UIAffineTransformMake(a: number, b: number, c: number, d: number, tx: number, ty: number): UIAffineTransform

/* Return a transform which translates by `(tx, ty)':
     t' = [ 1 0 0 1 tx ty ] */
UIAffineTransformMakeTranslation(tx: number, ty: number): UIAffineTransform

/* Return a transform which scales by `(sx, sy)':
     t' = [ sx 0 0 sy 0 0 ] */
UIAffineTransformMakeScale(sx: number, sy: number): UIAffineTransform

/* Return a transform which rotates by `angle' radians:
     t' = [ cos(angle) sin(angle) -sin(angle) cos(angle) 0 0 ] */
UIAffineTransformMakeRotation(angle: number): UIAffineTransform

/* Return true if `t' is the identity transform, false otherwise. */
UIAffineTransformIsIdentity(t: UIAffineTransform): boolean

/* Translate `t' by `(tx, ty)' and return the result:
     t' = [ 1 0 0 1 tx ty ] * t */
UIAffineTransformTranslate(t: UIAffineTransform, tx: number, ty: number): UIAffineTransform

/* Scale `t' by `(sx, sy)' and return the result:
     t' = [ sx 0 0 sy 0 0 ] * t */
UIAffineTransformScale(t: UIAffineTransform, sx: number, sy: number): UIAffineTransform

/* Rotate `t' by `angle' radians and return the result:
     t' =  [ cos(angle) sin(angle) -sin(angle) cos(angle) 0 0 ] * t */
UIAffineTransformRotate(t: UIAffineTransform, angle: number): UIAffineTransform

/* Invert `t' and return the result. If `t' has zero determinant, then `t'
   is returned unchanged. */
UIAffineTransformInvert(t: UIAffineTransform): UIAffineTransform

/* Concatenate `t2' to `t1' and return the result:
     t' = t1 * t2 */
UIAffineTransformConcat(t1: UIAffineTransform, t2: UIAffineTransform): UIAffineTransform

/* Return true if `t1' and `t2' are equal, false otherwise. */
UIAffineTransformEqualToTransform(t1: UIAffineTransform, t2: UIAffineTransform): UIAffineTransform

/**
 * The inset distances for views.
 */
UIEdgeInsets = {top: number, left: number, bottom: number, right: number}

/* The "zero" insets -- equivalent to UIEdgeInsetsMake(0, 0, 0, 0). */
UIEdgeInsetsZero: UIEdgeInsets

/**
 * Make an insets from `(top, left, bottom, right)'.
 */
UIEdgeInsetsMake(top: number, left: number, bottom: number, right: number): UIEdgeInsets

/* Adjusts a rectangle by the given edge insets. */
UIEdgeInsetsInsetRect(rect: UIRect, insets: UIEdgeInsets): UIRect

/* Return true if `t1' and `t2' are equal, false otherwise. */
UIEdgeInsetsEqualToEdgeInsets(rect1: UIEdgeInsets, rect2: UIEdgeInsets): boolean

/**
 * A structure used to describe a portion of a series, such as characters in a string or objects in an array.
 */
UIRange = {location: number, length: number}

/**
 * Make a range from `(location, length)'.
 */
UIRangeMake(location: number, length: number): UIRange

```