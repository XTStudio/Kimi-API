# UIKit | UIViewController

An object that manages a view hierarchy for your UIKit app.

```typescript

/**
 * A localized string that represents the view this controller manages.
 */
title: string

/**
 * The view that the controller manages.
 */
view: UIView

/**
 * The safeAreaInsets of view that the controller manages.
 */
safeAreaInsets: EdgeInsets

/**
 * Creates the view that the controller manages.
 */
loadView(): void

/**
 * A Boolean value indicating whether the view is currently loaded into memory. 
 */
viewDidLoad(): void

/**
 * Notifies the view controller that its view is about to be added to a view hierarchy. 
 */
viewWillAppear(animated: boolean): void

/**
 * Notifies the view controller that its view was added to a view hierarchy.
 */
viewDidAppear(animated: boolean): void

/**
 * Notifies the view controller that its view is about to be removed from a view hierarchy.
 */
viewWillDisappear(animated: boolean): void

/**
 * Notifies the view controller that its view was removed from a view hierarchy.
 */
viewDidDisappear(animated: boolean): void

/**
 * Called to notify the view controller that its view is about to layout its subviews.
 */
viewWillLayoutSubviews(): void

/**
 * Calls after viewWillLayoutSubviews invoke.
 */
on('viewWillLayoutSubviews', (sender: UIViewController) => void): void

/**
 * Called to notify the view controller that its view has just laid out its subviews.
 */
viewDidLayoutSubviews(): void

/**
 * The parent view controller of the recipient.
 */
readonly parentViewController: UIViewController | undefined

/**
 * The view controller that is presented by this view controller, or one of its ancestors in the view controller hierarchy.
 */
readonly presentedViewController: UIViewController | undefined

/**
 * The view controller that presented this view controller.
 */
readonly presentingViewController: UIViewController | undefined

/**
 * Presents a view controller modally.
 */
presentViewController(viewController: UIViewController, animated?: boolean, completion?: () => void): void

/**
 * Dismisses the view controller that was presented modally by the view controller.
 */
dismissViewController(animated?: boolean, completion?: () => void): void

/**
 * An array of view controllers that are children of the current view controller.
 */
readonly childViewControllers: UIViewController[]

/**
 * Adds the specified view controller as a child of the current view controller.
 */
addChildViewController(viewController: UIViewController): void

/**
 * Removes the view controller from its parent.
 */
removeFromParentViewController(): void

/**
 * Called just before the view controller is added or removed from a container view controller.
 */
willMoveToParentViewController(parent?: UIViewController): void

/**
 * Called after the view controller is added or removed from a container view controller.
 */
didMoveToParentViewController(parent?: UIViewController): void

/**
 * The nearest ancestor in the view controller hierarchy that is a navigation controller.
 */
readonly navigationController: UINavigationController | undefined

/**
 * Return current UINavigationItem.
 */
readonly navigationItem: UINavigationItem

/**
 * The nearest ancestor in the view controller hierarchy that is a tab bar controller.
 */
readonly tabBarController: UITabBarController

/**
 * Return current UITabBarItem.
 */
readonly tabBarItem: UITabBarItem

```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uiviewcontroller?language=objc)
* [UINavigationController](UINavigationController.md)
* [UINavigationItem](UINavigationItem.md)
* [UITabBarController](UITabBarController.md)
* [UITabBarItem](UITabBarItem.md)