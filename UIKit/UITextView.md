# UIKit > UITextView extends UIScrollView

A scrollable, multiline text region.

```typescript

/**
 * The text displayed by the text field.
 */
text: string | undefined

/**
 * The color of the text.
 */
textColor: UIColor | undefined

/**
 * The font of the text.
 */
font: UIFont | undefined

/**
 * The technique to use for aligning the text.
 */
textAlignment: UITextAlignment

/**
 * A Boolean value indicating whether the receiver is editable.
 */
editable: boolean

/**
 * A Boolean value indicating whether the receiver is selectable.
 */
selectable: boolean

/**
 * A Boolean value indicating whether the text field is currently in edit mode.
 */
readonly editing: boolean

/**
 * Scrolls the receiver until the text in the specified range is visible.
 */
scrollRangeToVisible(range: Range): void

/**
 * let UITextView start editing.
 */
focus(): void

/**
 * let UITextView end editing.
 */
blur(): void

/**
 * The auto-capitalization style for the text object.
 */
autocapitalizationType: UITextAutocapitalizationType

/**
 * The autocorrection style for the text object.
 */
autocorrectionType: UITextAutocorrectionType

/**
 * The spell-checking style for the text object.
 */
spellCheckingType: UITextSpellCheckingType

/**
 * The keyboard style associated with the text object.
 */
keyboardType: UIKeyboardType

/**
 * The visible title of the Return key.
 */
returnKeyType: UIReturnKeyType

/**
 * Identifies whether the text object should disable text copying and in some cases hide the text being entered.
 */
secureTextEntry: boolean

/**
 * Asks if editing should begin in the specified text view.
 */
on('shouldBeginEditing', (sender: UITextView) => boolean): void

/**
 * Tells that editing of the specified text view has begun.
 */
on('didBeginEditing', (sender: UITextView) => void): void

/**
 * Asks if editing should stop in the specified text view.
 */
on('shouldEndEditing', (sender: UITextView) => boolean): void

/**
 * Tells that editing of the specified text view has ended.
 */
on('didEndEditing', (sender: UITextView) => void): void

/**
 * Asks whether the specified text should be replaced in the text view.
 */
on('shouldChange', (sender: UITextView, charactersInRange: Range, replacementString: string) => boolean): void
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uitextview?language=objc)
* [Range / UITextAlignment / UITextAutocapitalizationType / UITextAutocorrectionType / UITextSpellCheckingType / UIKeyboardType / UIReturnKeyType](Enums.md)
* [UIColor](UIColor.md)
* [UIFont](UIFont.md)