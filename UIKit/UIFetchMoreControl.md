# UIKit | UIFetchMoreControl extends UIView

```typescript

/**
 * A Boolean value indicating whether a fetch operation sholud be trigger. 
 */
enabled: boolean

/**
 * A Boolean value indicating whether a fetch operation has been triggered and is in progress. 
 */
readonly fetching: boolean

/**
 * The tint color for the fetch control.
 */
tintColor: UIColor | undefined

/**
 * Tells the control that a fetch operation was started programmatically.
 */
beginFetching(): void

/**
 * Tells the control that a fetch operation has ended.
 */
endFetching(): void

/**
 * Trigger when user drag scroll view to active fetch control.
 */
on('fetch', (sender: UIRefreshControl) => void): void

```

