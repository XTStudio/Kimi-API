# UIKit | UINavigationBar extends UIView

```typescript

/**
 * A Boolean value indicating whether the navigation bar is translucent (YES) or not (NO).
 */
translucent: boolean

/**
 * The tint color to apply to the navigation bar background.
 */
barTintColor: UIColor | undefined

/**
 * Display attributes for the bar’s title text.
 */
titleTextAttributes: {[key: string]: any}   // key: UIAttributedStringKey

/**
 * The image shown beside the back button.
 */
backIndicatorImage: UIImage | undefined

/**
 * The image used as a mask for content during push and pop transitions.
 */
backIndicatorTransitionMaskImage: UIImage | undefined

```

## Relate

* [UIAttributedStringKey](UIAttributedString.md)
* [UIColor](UIColor.md)
* [UIImage](UIImage.md)