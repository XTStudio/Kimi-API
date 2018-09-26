# UIKit | UIPasteboard

An object that helps a user share data from one place to another within your app, and from your app to other apps.

```typescript

/**
 * Returns the systemwide general pasteboard, which is used for general copy-paste operations
 */
static readonly shared: UIPasteboard

/**
 * The string value of the first pasteboard item.
 */
string: string | undefined

```