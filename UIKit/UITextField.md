# UIKit | UITextField extends UIView

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
 * The string that is displayed when there is no other text in the text field.
 */
placeholder: string | undefined

/**
 * A Boolean value indicating whether the text field removes old text when editing begins.
 */
clearsOnBeginEditing: boolean

/**
 * A Boolean value indicating whether the text field is currently in edit mode.
 */
readonly editing: boolean

/**
 * Controls when the standard clear button appears in the text field.
 */
clearButtonMode: UITextFieldViewMode

/**
 * The overlay view displayed on the left (or leading) side of the text field.
 */
leftView: UIView | undefined

/**
 * Controls when the left overlay view appears in the text field.
 */
leftViewMode: UITextFieldViewMode

/**
 * The overlay view displayed on the right (or trailing) side of the text field.
 */
rightView: UIView | undefined

/**
 * Controls when the right overlay view appears in the text field.
 */
rightViewMode: UITextFieldViewMode

/**
 * A Boolean value indicating whether inserting text replaces the previous contents.
 */
clearsOnInsertion: boolean 

/**
 * let UITextField start editing.
 */
focus(): void

/**
 * let UITextField end editing.
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
 * Asks if editing should begin in the specified text field.
 */
on('shouldBeginEditing', (sender: UITextField) => boolean): void

/**
 * Tells that editing began in the specified text field.
 */
on('didBeginEditing', (sender: UITextField) => void): void

/**
 * Asks if editing should stop in the specified text field.
 */
on('shouldEndEditing', (sender: UITextField) => boolean): void

/**
 * Tells that editing stopped for the specified text field.
 */
on('didEndEditing', (sender: UITextField) => void): void

/**
 * Asks if the specified text should be changed.
 */
on('shouldChange', (sender: UITextField, charactersInRange: Range, replacementString: string) => boolean): void

/**
 * Asks if the text field’s current contents should be removed.
 */
on('shouldClear', (sender: UITextField) => boolean): void

/**
 * Asks if the text field should process the pressing of the return button.
 */
on('shouldReturn', (sender: UITextField) => boolean): void
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uitextfield?language=objc)
* [Range / UITextAlignment / UITextFieldViewMode / UITextAutocapitalizationType / UITextAutocorrectionType / UITextSpellCheckingType / UIKeyboardType / UIReturnKeyType](Enums.md)
* [UIColor](UIColor.md)
* [UIFont](UIFont.md)