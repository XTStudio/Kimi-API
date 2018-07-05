# UIKit | UIProgressView extends UIView

A view that depicts the progress of a task over time.

```typescript

/**
 * The current progress shown by the receiver.
 */
progress: number

/**
 * Adjusts the current progress shown by the receiver, optionally animating the change.
 */
setProgress(value: number, animated: boolean): void

/**
 * The color shown for the portion of the progress bar that is filled.
 */
progressTintColor: UIColor | undefined

/**
 * The color shown for the portion of the progress bar that is not filled.
 */
trackTintColor: UIColor | undefined

```

## Relate

* [UIColor](UIColor.md)