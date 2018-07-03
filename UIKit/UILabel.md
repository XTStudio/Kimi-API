# UIKit | UILabel extends UIView

A view that displays one or more lines of read-only text, often used in conjunction with controls to describe their intended purpose.

```typescript
/**
 * The current text that is displayed by the label.
 */
text: string | undefined

/**
 * The current styled text that is displayed by the label.
 */
attributedText: UIAttributedString | undefined

/**
 * The font used to display the text.
 */
font: UIFont | undefined

/**
 * The color of the text.
 */
textColor: UIColor | undefined

/**
 * The technique to use for aligning the text.
 */
textAlignment: UITextAlignment

/**
 * The technique to use for wrapping and truncating the label’s text.
 */
lineBreakMode: UILineBreakMode

/**
 * The maximum number of lines to use for rendering text.
 */
numberOfLines: number
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uilabel?language=objc)
* [UIAttributedString](UIAttributedString.md)
* [UIFont](UIFont.md)
* [UIColor](UIColor.md)
* [UITextAlignment / UILineBreakMode](Enums.md)