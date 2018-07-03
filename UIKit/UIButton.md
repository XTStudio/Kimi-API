# UIKit > UIButton extends UIView

A control that executes your custom code in response to user interactions.

```typescript
/**
 * system button provides preset actions, such as highlight text color and image adjusting.
 * set isCustomm to true to disable these preset actions.
 */
constructor(isCustom?: boolean = false)

/**
 * A Boolean value indicating whether the control is enabled.
 */
enabled: boolean

/**
 * A Boolean value indicating whether the control is in the selected state.
 */
selected: boolean

/**
 * A Boolean value indicating whether the control draws a highlight.
 */
readonly highlighted: boolean

/**
 * A Boolean value indicating whether the control is currently tracking touch events.
 */
readonly tracking: boolean

/**
 * A Boolean value indicating whether a tracked touch event is currently inside the control’s bounds.
 */
readonly touchInside: boolean

/**
 * The vertical alignment of content within the control’s bounds.
 */
contentVerticalAlignment: UIControlContentVerticalAlignment

/**
 * The horizontal alignment of content within the control’s bounds.
 */
contentHorizontalAlignment: UIControlContentHorizontalAlignment

/**
 * Sets the title to use for the specified state.
 */
setTitle(title?: string, state: UIControlState): void

/**
 * Sets the color of the title to use for the specified state.
 */
setTitleColor(color?: UIColor, state: UIControlState): void

/**
 * Sets the font of the title to use for the specified state.
 */
setTitleFont(font: UIFont): void

/**
 * Sets the image to use for the specified state.
 */
setImage(image?: UIImage, state: UIControlState): void

/**
 * Sets the styled title to use for the specified state.
 */
setAttributedTitle(title?: UIAttributedString, state: UIControlState): void

/**
 * The inset or outset margins for the rectangle surrounding all of the button’s content.
 */
contentEdgeInsets: EdgeInsets

/**
 * The inset or outset margins for the rectangle around the button’s title text.
 */
titleEdgeInsets: EdgeInsets

/**
 * The inset or outset margins for the rectangle around the button’s image.
 */
imageEdgeInsets: EdgeInsets

/**
 * You use touchDown event to handle touch-down event in the control.
 */
on('touchDown', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle repeated touch-down event in the control.
 */
on('touchDownRepeat', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle a finger is dragged inside the bounds of the control.
 */
on('touchDragInside', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle a finger is dragged just outside the bounds of the control.
 */
on('touchDragOutside', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle a finger is dragged into the bounds of the control. 
 */
on('touchDragEnter', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle a finger is dragged from within a control to outside its bounds.
 */
on('touchDragExit', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle a touch-up event in the control where the finger is inside the bounds of the control.
 */
on('touchUpInside', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle a touch-up event in the control where the finger is outside the bounds of the control.
 */
on('touchUpOutside', (sender: UIButton) => void): void

/**
 * You use touchDown event to handle a system event canceling the current touches for the control.
 */
on('touchCancel', (sender: UIButton) => void): void
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uibutton?language=objc)
* [UIControlState / UIControlContentVerticalAlignment / UIControlContentHorizontalAlignment](Enums.md)
* [EdgeInsets](Interfaces.md)
* [UIColor](UIColor.md)
* [UIFont](UIFont.md)
* [UIImage](UIImage.md)
* [UIAttributedString](UIAttributedString.md)