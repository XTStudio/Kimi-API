# UIKit | UIActivityIndicatorView extends UIView

A view that shows that a task is in progress.

```typescript
/**
 * The color of the activity indicator.
 */
color: UIColor

/**
 * The size of the activity indicator, large size if true.
 */
largeStyle: boolean

/**
 * A Boolean value indicating whether the activity indicator is currently running its animation.
 */
readonly animating: boolean

/**
 * Starts the animation of the progress indicator.
 */
startAnimating(): void

/**
 * Stops the animation of the progress indicator.
 */
stopAnimating(): void
```

## Relate

* [UIColor](UIColor.md)