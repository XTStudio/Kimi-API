# UIKit | UIAttributedString

## UIAttributedStringKey

```typescript
const UIForegroundColorAttributeName: string      // value: UIColor
const UIFontAttributeName: string                 // value: UIFont
const UIBackgroundColorAttributeName: string      // value: UIColor
const UIKernAttributeName: string                 // value: number
const UIStrikethroughStyleAttributeName: string   // value: number
const UIUnderlineStyleAttributeName: string       // value: number
const UIStrokeColorAttributeName: string          // value: UIColor
const UIStrokeWidthAttributeName: string          // value: number
const UIUnderlineColorAttributeName: string       // value: UIColor
const UIStrikethroughColorAttributeName: string   // value: UIColor
```

## UIAttributedString

A string that has associated attributes (such as visual style, hyperlinks, or accessibility data) for portions of its text.

```typescript
/**
 * Returns an UIAttributedString object initialized with a given string and attributes.
 */
constructor(str: string, attributes: {[key: string]: any})  // attributes -> key: UIAttributedStringKey

/**
 * Returns an UIMutableAttributedString object instance with this string and attributes.
 */
mutable(): UIMutableAttributedString
```

## UIMutableAttributedString extends UIAttributedString

```typescript
/**
 * Returns an UIMutableAttributedString object initialized with a given string and attributes.
 */
constructor(str: string, attributes: {[key: string]: any})  // attributes -> key: UIAttributedStringKey

/**
 * Replaces the characters in the given range with the characters of the given string.
 */
replaceCharacters(inRange: Range, withString: string): void

/**
 * Sets the attributes for the characters in the specified range to the specified attributes.
 */
setAttributes(attributes: {[key: string]: any}, range: Range): void

/**
 * Adds an attribute with the given name and value to the characters in the specified range.
 */
addAttribute(attrName: string, value: any, range: Range): void

/**
 * Adds the given collection of attributes to the characters in the specified range.
 */
addAttributes(attributes: {[key: string]: any}, range: Range): void

/**
 * Removes the named attribute from the characters in the specified range.
 */
removeAttribute(attrName: string, range: Range): void

/**
 * Replaces the characters and attributes in a given range with the characters and attributes of the given attributed string.
 */
replaceCharactersWithAttributedString(inRange: Range, withAttributedString: UIAttributedString): void

/**
 * Inserts the characters and attributes of the given attributed string into the receiver at the given index.
 */
insertAttributedString(attributedString: UIAttributedString, atIndex: number): void

/**
 * Adds the characters and attributes of a given attributed string to the end of the receiver.
 */
appendAttributedString(attributedString: UIAttributedString): void

/**
 * Deletes the characters in the given range along with their associated attributes.
 */
deleteCharacters(inRange: Range): void

/**
 * Returns an UIAttributedString object instance with this string and attributes.
 */
immutable(): UIAttributedString
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/foundation/nsattributedstring?language=objc)
* [Range](Enums.md)