# UIKit | UIGestureRecognizer

## UIGestureRecognizerState

```typescript
enum UIGestureRecognizerState {
    /**
     * The gesture recognizer has not yet recognized its gesture, but may be evaluating touch events. This is the default state.
     */
    possible

    /**
     * The gesture recognizer has received touch objects recognized as a continuous gesture. It sends its action message (or messages) at the next cycle of the run loop.
     */
    began

    /**
     * The gesture recognizer has received touches recognized as a change to a continuous gesture. It sends its action message (or messages) at the next cycle of the run loop.
     */
    changed

    /**
     * The gesture recognizer has received touches recognized as the end of a continuous gesture. It sends its action message (or messages) at the next cycle of the run loop and resets its state to possible.
     */
    ended

    /**
     * The gesture recognizer has received touches resulting in the cancellation of a continuous gesture. It sends its action message (or messages) at the next cycle of the run loop and resets its state to possible.
     */
    cancelled

    /**
     * The gesture recognizer has received a multi-touch sequence that it cannot recognize as its gesture. No action message is sent and the gesture recognizer is reset to possible.
     */
    failed
}
```

## UIGestureRecognizer

```typescript
/**
 * The current state of the gesture recognizer.
 */
readonly state: UIGestureRecognizerState

/**
 * A Boolean property that indicates whether the gesture recognizer is enabled.
 */
enabled: boolean

/**
 * The view the gesture recognizer is attached to.
 */
readonly view: UIView | undefined

/**
 * A Boolean indicating whether the gesture recognizer considers touches of different types simultaneously.
 */
requiresExclusiveTouchType: boolean

/**
 * Creates a dependency relationship between the receiver and another gesture recognizer when the objects are created.
 */
requireGestureRecognizerToFail(otherGestureRecognizer: UIGestureRecognizer): void

/**
 * Returns the point computed as the location in a given view of the gesture represented by the receiver.
 */
locationInView(view: UIView): Point
```

## UITapGestureRecognizer: UIGestureRecognizer

```typescript
/**
 * The number of taps for the gesture to be recognized.
 */
numberOfTapsRequired: number = 1

/**
 * The number of fingers required to tap for the gesture to be recognized.
 */
numberOfTouchesRequired: number = 1

/**
 * You use touch event to handle tap.
 */
on('touch', (sender: UITapGestureRecognizer) => void): this
```

## UILongPressGestureRecognizer: UIGestureRecognizer

```typescript

/**
 * The number of taps for the gesture to be recognized.
 */
numberOfTapsRequired: number = 0

/**
 * The number of fingers required to tap for the gesture to be recognized.
 */
numberOfTouchesRequired: number = 1

/**
 * The minimum period fingers must press on the view for the gesture to be recognized.
 */
minimumPressDuration: number = 0.5

/**
 * The maximum movement of the fingers on the view before the gesture fails.
 */
allowableMovement: number = 10

/**
 * You use began event to handle a LongPressGesture began.
 */
on('began', (sender: UILongPressGestureRecognizer) => void): this

/**
 * You use changed event to handle a LongPressGesture moved(finger move).
 */
on('changed', (sender: UILongPressGestureRecognizer) => void): this

/**
 * You use ended event to handle a LongPressGesture ended(finger up).
 */
on('ended', (sender: UILongPressGestureRecognizer) => void): this

/**
 * You use cancelled event to handle a LongPressGesture was cancelled by another responder.
 */
on('cancelled', (sender: UILongPressGestureRecognizer) => void): this
```

## UIPanGestureRecognizer: UIGestureRecognizer

```typescript
/**
 * The minimum number of fingers that can be touching the view for this gesture to be recognized.
 */
minimumNumberOfTouches: number = 1

/**
 * The maximum number of fingers that can be touching the view for this gesture to be recognized.
 */
maximumNumberOfTouches: number = Infinite

/**
 * The translation of the pan gesture in the coordinate system of the specified view.
 */
translationInView:(view?: UIView): Point

/**
 * Sets the translation value in the coordinate system of the specified view.
 */
setTranslation:(translate: Point, inView?: UIView): void

/**
 * The velocity of the pan gesture in the coordinate system of the specified view.
 */
velocityInView:(view?: UIView): Point

/**
 * You use began event to handle a PanGesture began.
 */
on('began', (sender: UIPanGestureRecognizer) => void): this

/**
 * You use changed event to handle a PanGesture moved(finger move).
 */
on('changed', (sender: UIPanGestureRecognizer) => void): this

/**
 * You use ended event to handle a PanGesture ended(finger up).
 */
on('ended', (sender: UIPanGestureRecognizer) => void): this

/**
 * You use cancelled event to handle a PanGesture was cancelled by another responder.
 */
on('cancelled', (sender: UIPanGestureRecognizer) => void): this
```

## UIPinchGestureRecognizer: UIGestureRecognizer

```typescript
/**
 * The scale factor relative to the points of the two touches in screen coordinates.
 */
scale: number

/**
 * The velocity of the pinch in scale factor per second.
 */
readonly velocity: number

/**
 * You use began event to handle a PinchGesture began.
 */
on('began', (sender: UIPinchGestureRecognizer) => void): this

/**
 * You use changed event to handle a PinchGesture moved(fingers move).
 */
on('changed', (sender: UIPinchGestureRecognizer) => void): this

/**
 * You use ended event to handle a PinchGesture ended(fingers up).
 */
on('ended', (sender: UIPinchGestureRecognizer) => void): this

/**
 * You use cancelled event to handle a PinchGesture was cancelled by another responder.
 */
on('cancelled', (sender: UIPinchGestureRecognizer) => void): this
```

## UIRotationGestureRecognizer: UIGestureRecognizer

```typescript
/**
 * The rotation of the gesture in radians.
 */
rotation: number

/**
 * The velocity of the rotation gesture in radians per second.
 */
readonly velocity: number

/**
 * You use began event to handle a RotateGesture began.
 */
on('began', (sender: UIRotationGestureRecognizer) => void): this

/**
 * You use changed event to handle a RotateGesture moved(fingers move).
 */
on('changed', (sender: UIRotationGestureRecognizer) => void): this

/**
 * You use ended event to handle a RotateGesture ended(fingers up).
 */
on('ended', (sender: UIRotationGestureRecognizer) => void): this

/**
 * You use cancelled event to handle a RotateGesture was cancelled by another responder.
 */
on('cancelled', (sender: UIRotationGestureRecognizer) => void): this
```

## Relate

* [Point](Interfaces.md)