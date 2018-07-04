# UIKit | UITabBarController extends UIViewController

```typescript

/**
 * The index of the view controller associated with the currently selected tab item.
 */
selectedIndex: number

/**
 * The view controller associated with the currently selected tab item.
 */
selectedViewController: UIViewController | undefined

/**
 * Replaces the view controllers currently managed by the navigation controller with the specified items.
 */
setViewControllers(viewControllers: UIViewController[], animated?: boolean): void

/**
 * The tab bar view associated with this controller.
 */
readonly tabBar: UITabBar

```

## Relate

* [UIViewController](UIViewController.md)
* [UITabBar](UITabBar.md)