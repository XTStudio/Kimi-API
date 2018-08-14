# UIKit | UIRefreshControl extends UIView

```typescript

/**
 * A Boolean value indicating whether a refresh operation sholud be trigger. 
 */
enabled: boolean

/**
 * A Boolean value indicating whether a refresh operation has been triggered and is in progress. 
 */
readonly refreshing: boolean

/**
 * The tint color for the refresh control.
 */
tintColor: UIColor | undefined

/**
 * Tells the control that a refresh operation was started programmatically.
 */
beginRefreshing(): void

/**
 * Tells the control that a refresh operation has ended.
 */
endRefreshing(): void

/**
 * Trigger when user drag scroll view to active refresh control.
 */
on('refresh', (sender: UIRefreshControl) => void): void

```

