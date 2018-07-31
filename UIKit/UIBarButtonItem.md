# UIKit | UIBarButtonItem

A button specialized for placement on a toolbar or tab bar.

```typescript

/**
 * The title of the item.
 */
title: string | undefined

/**
 * The title's style of the item.
 */
titleAttributes: {[key: string]: any}   // key: UIAttributedStringKey

/**
 * The icon of the item.
 */
image: UIImage | undefined

/**
 * The tint color to apply to the button item.
 */
tintColor: UIColor

/**
 * The width of the item.
 */
width: number

/**
 * The custom-view of the item.
 */
customView: UIView | undefined

/**
 * Call after user tap bar button.
 */
on('touchUpInside', (sender: UIBarButtonItem) => void): this

```

* [UIAttributedStringKey](UIAttributedString.md)
* [UIColor](UIColor.md)
* [UIImage](UIImage.md)