# UIKit | UIWebView extends UIView

An object that displays interactive web content, such as for an in-app browser.

```typescript
/**
 * The page title.
 */
readonly title: string | undefined

/**
 * The active URL.
 */
readonly URL: URL | undefined

/**
 * A Boolean value indicating whether the view is currently loading content.
 */
readonly loading: boolean

/**
 * Navigates to a requested URL.
 */
loadRequest(request: URLRequest): void

/**
 * Sets the webpage contents and base URL.
 */
loadHTMLString(HTMLString: string, baseURL: URL): void

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
on('newRequest', (request: URLRequest) => boolean): this

/**
 * Calls after web page start loading.
 */
on('didStart', () => void): this

/**
 * Calls after web page finish loading.
 */
on('didFinish', () => void): this

/**
 * Calls after web page fail to load.
 */
on('didFail', (error: Error) => void): this

/**
 * Calls after webview post message to application using 'KIMI.postMessage(message, handler:() => void)'.
 */
on('message', (message: string, callback?: (...arguments: any[]) => void) => void): this
```
