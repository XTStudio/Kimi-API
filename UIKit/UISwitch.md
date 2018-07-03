# UIKit > UISwitch extends UIView

A control that offers a binary choice, such as On/Off.

```typescript
/**
 * The color used to tint the appearance of the switch when it is turned on.
 */
onTintColor: UIColor | undefined

/**
 * The color used to tint the appearance of the thumb.
 */
thumbTintColor: UIColor | undefined

/**
 * A Boolean value that determines the off/on state of the switch.
 */
isOn: boolean

/**
 * Set the state of the switch to On or Off, optionally animating the transition.
 */
setOn(on: boolean, animated: boolean): void

/**
 * Calls after on state changed by user taps.
 */
on('valueChanged', (sender: UISwitch) => void): void
```

## Relate

* [UIColor](UIColor.md)