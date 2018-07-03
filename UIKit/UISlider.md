# UIKit | UISlider extends UIView

A control used to select a single value from a continuous range of values.

```typescript
/**
 * The slider’s current value.
 */
value: number = 0.0

/**
 * The minimum value of the slider.
 */
minimumValue: number = 0.0

/**
 * The maximum value of the slider.
 */
maximumValue: number = 1.0

/**
 * The color used to tint the default minimum track images.
 */
minimumTrackTintColor: UIColor | undefined

/**
 * The color used to tint the default maximum track images.
 */
maximumTrackTintColor: UIColor | undefined

/**
 * The color used to tint the default thumb images.
 */
thumbTintColor: UIColor | undefined

/**
 * Sets the slider’s current value, allowing you to animate the change visually.
 */
setValue(value: number, animated: boolean): void

/**
 * Calls after value changed by user drags.
 */
on('valueChanged', (sender: UISlider) => void): void
```

## Relate

* [UIColor](UIColor.md)