# UIKit | UINavigationController extends UIViewController

```typescript

/**
 * Initializes and returns a newly created navigation controller.
 */
constructor(rootViewController?: UIViewController)

/**
 * Pushes a view controller onto the receiver’s stack and updates the display.
 */
pushViewController(viewController: UIViewController, animated?: boolean): void

/**
 * Pops the top view controller from the navigation stack and updates the display.
 */
popViewController(animated?: boolean): UIViewController | undefined

/**
 * Pops view controllers until the specified view controller is at the top of the navigation stack.
 */
popToViewController(viewController: UIViewController, animated?: boolean): UIViewController[]

/**
 * Pops all the view controllers on the stack except the root view controller and updates the display.
 */
popToRootViewController(animated?: boolean): UIViewController[]

/**
 * Replaces the view controllers currently managed by the navigation controller with the specified items.
 */
setViewControllers(viewControllers: UIViewController[], animated?: boolean): void

/**
 * The navigation bar managed by the navigation controller.
 */
readonly navigationBar: UINavigationBar

/**
 * Sets whether the navigation bar is hidden.
 */
setNavigationBarHidden(hidden: boolean, animated: boolean): void

```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uinavigationcontroller?language=objc)
* [UIViewController](UIViewController.md)
* [UINavigationBar](UINavigationBar.md)