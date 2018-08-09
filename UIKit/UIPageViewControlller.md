# UIKit | UIPageViewController extends UIViewController

A container view controller that manages navigation between pages of content, where each page is managed by a child view controller.

```typescript

/**
 * Initializes a newly created page view controller. 
 */
constructor(isVertical?: boolean)

/**
 * If page-items setted, and loops sets to true, the page-viewcontroller enters infinite loops mode.
 * eg: when user scroll to last page, the next page is the page-items first page.
 */
loops: boolean = false

/**
 * Set static items for page-viewcontroller.
 */
pageItems: UIViewController[]

/**
 * Sets current page.
 */
currentPage: UIViewController | undefined

/**
 * Scrolls to next page.
 */
scrollToNextPage(animated?: boolean = true): void

/**
 * Scrolls to previous page.
 */
scrollToPreviousPage(animated?: boolean = true): void

/**
 * Returns the view controller before the given view controller.
 */
on('beforeViewController', (currentPage: UIViewController) => UIViewController | undefined): this

/**
 * Returns the view controller after the given view controller.
 */
on('afterViewController', (currentPage: UIViewController) => UIViewController | undefined): this

/**
 * Called after a gesture-driven transition completes.
 */
on('didFinishAnimating', (currentPage: UIViewController, previousPages: UIViewController[]) => void): this

```
