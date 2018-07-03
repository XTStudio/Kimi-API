# UIKit > UIWebView extends UIView

An object that displays interactive web content, such as for an in-app browser.

```typescript
/**
 * The page title.
 */
readonly title: string | undefined

/**
 * The active URL.
 */
readonly URL: NSURL | undefined

/**
 * A Boolean value indicating whether the view is currently loading content.
 */
readonly loading: boolean

/**
 * Navigates to a requested URL.
 */
loadRequest(request: NSURLRequest): void

/**
 * Sets the webpage contents and base URL.
 */
loadHTMLString(HTMLString: string, baseURL: NSURL): void

/**
 * Navigates to the back item in the back-forward list.
 */
goBack(): void

/**
 * Navigates to the forward item in the back-forward list.
 */
goForward(): void

/**
 * Reloads the current page.
 */
reload(): void

/**
 * Stops loading all resources on the current page.
 */
stopLoading(): void

/**
 * Evaluates a JavaScript string.
 */
evaluateJavaScript(script: string, completed: (result?: any, error?: Error) => void): void

/**
 * Tells the delegate if a new request should be accepted.
 */
on('newRequest', (request: NSURLRequest) => boolean): void

/**
 * Calls after web page start loading.
 */
on('didStart', () => void): void

/**
 * Calls after web page finish loading.
 */
on('didFinish', () => void): void

/**
 * Calls after web page fail to load.
 */
on('didFail', (error: Error) => void): void
```