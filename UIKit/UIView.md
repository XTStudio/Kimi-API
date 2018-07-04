# UIKit | UIView

An object that manages the content for a rectangular area on the screen.

```typescript

constructor(): UIView

/**
 * A backface of UIView
 */
readonly layer: CALayer

// Geometry

/**
 * The frame rectangle, which describes the view’s location and size in its superview’s coordinate system.
 * @see https://developer.apple.com/documentation/uikit/uiview/1622621-frame?language=objc
 */
frame: Rect

/**
 * The bounds rectangle, which describes the view’s location and size in its own coordinate system.
 * @see https://developer.apple.com/documentation/uikit/uiview/1622580-bounds?language=objc
 */
bounds: Rect

/**
 * The center point of the view's frame rectangle.
 * @see https://developer.apple.com/documentation/uikit/uiview/1622627-center?language=objc
 */
center: Point

/**
 * Specifies the transform applied to the view, relative to the center of its bounds.
 * @see https://developer.apple.com/documentation/uikit/uiview/1622459-transform?language=objc
 */
transform: AffineTransform

// Hierarchy

/**
 * An integer that you can use to identify view objects in your application.
 */
tag: number = 0

/**
 * The receiver’s superview, or nil if it has none.
 */
readonly superview: UIView | undefined

/**
 * The receiver’s immediate subviews.
 */
readonly subviews: UIView[]

/**
 * Unlinks the view from its superview and its window, and removes it from the responder chain.
 */
removeFromSuperview(): void

/**
 * Inserts a subview at the specified index.
 */
insertSubviewAtIndex(view: UIView, index: number): void

/**
 * Exchanges the subviews at the specified indices.
 */
exchangeSubview(index1: number, index2: number): void

/**
 * Adds a view to the end of the receiver’s list of subviews.
 */
addSubview(view: UIView): void

/**
 * Inserts a view below another view in the view hierarchy.
 */
insertSubviewBelowSubview(view: UIView, belowSubview: UIView): void

/**
 * Inserts a view above another view in the view hierarchy.
 */
insertSubviewAboveSubview(view: UIView, aboveSubview: UIView): void

/**
 * Moves the specified subview so that it appears on top of its siblings.
 */
bringSubviewToFront(view: UIView): void

/**
 * Moves the specified subview so that it appears behind its siblings.
 */
sendSubviewToBack(view: UIView): void

/**
 * Returns a Boolean value indicating whether the receiver is a subview of a given view or identical to that view.
 */
isDescendantOfView(view: UIView): boolean

/**
 * Returns the view whose tag matches the specified value.
 */
viewWithTag(tag: number): UIView | undefined

// Delegates

/**
 * Tells the view that a subview was added.
 */
didAddSubview(subview: UIView): void

/**
 * Tells the view that a subview is about to be removed.
 */
willRemoveSubview(subview: UIView): void

/**
 * Tells the view that its superview is about to change to the specified superview.
 */
willMoveToSuperview(newSuperview: UIView): void

/**
 * Tells the view that its superview changed.
 */
didMoveToSuperview(): void

/**
 * Invalidates the current layout of the receiver and triggers a layout update during the next update cycle.
 */
setNeedsLayout(): void

/**
 * Lays out the subviews immediately, if layout updates are pending.
 */
layoutIfNeeded(): void

/**
 * Lays out subviews.
 */
layoutSubviews(): void

// Rendering

/**
 * Marks the receiver’s entire bounds rectangle as needing to be redrawn.
 */
setNeedsDisplay(): void

/**
 * A Boolean value that determines whether subviews are confined to the bounds of the view.
 */
clipsToBounds: boolean

/**
 * The view’s background color.
 */
backgroundColor: UIColor | undefined

/**
 * The view’s alpha value.
 */
alpha: number

/**
 * A Boolean value that determines whether the view is hidden.
 */
hidden: boolean

/**
 * A flag used to determine how a view lays out its content when its bounds change.
 */
contentMode: UIViewContentMode

/**
 * The first nondefault tint color value in the view’s hierarchy, ascending from and starting with the view itself.
 */
tintColor: UIColor

/**
 * Called by the system when the tintColor property changes.
 */
tintColorDidChange(): void

// GestureRecognizers

/**
 * A Boolean value that determines whether user events are ignored and removed from the event queue.
 */
userInteractionEnabled: boolean

/**
 * The gesture-recognizer objects currently attached to the view.
 */
gestureRecognizers: UIGestureRecognizer[]

/**
 * Attaches a gesture recognizer to the view.
 */
addGestureRecognizer(gestureRecognizer: UIGestureRecognizer): void

/**
 * Detaches a gesture recognizer from the receiving view.
 */
removeGestureRecognizer(gestureRecognizer: UIGestureRecognizer): void

```

## Relates

* [Apple Document](https://developer.apple.com/documentation/uikit/uiview?language=objc)
* [Rect / Point / AffineTransform](Interfaces.md)
* [UIViewContentMode](Enums.md)
* [UIGestureRecognizer](UIGestureRecognizer.md)
* [UIColor](UIColor.md)