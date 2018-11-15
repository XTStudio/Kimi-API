# API

XT framework exposes iOS / Android / Web features.

includes the following frameworks.

* Foundation
* UIKit
* CoreGraphics

## Common

### EventEmitter

All objects extends [EventEmitter](https://github.com/Olical/EventEmitter), that means you could listen via EventEmitter, and emit event to objects.

### Never NULL

Kimi will not accept null as argument and return value, optional value will be ```undefined```.

## KIMI

Access KIMI APIs.

* [KMCore](Kimi/KMCore.md)

## Foundation

Access essential data types, collections, and operating-system services to define the base layer of functionality for your app.

* [Bundle](Foundation/Bundle.md)
* [Data](Foundation/Data.md)
* [DispatchQueue](Foundation/DispatchQueue.md)
* [FileManager](Foundation/FileManager.md)
* [Timer](Foundation/Timer.md)
* [URL](Foundation/URL.md)
* [URLRequest](Foundation/URLRequest.md)
* [URLResponse](Foundation/URLResponse.md)
* [URLSession](Foundation/URLSession.md)
* [UserDefaults](Foundation/UserDefaults.md)
* [UUID](Foundation/UUID.md)

## UIKit

Construct and manage a graphical, event-driven user interface for your app.

### Types

* [Enums](UIKit/Enums.md)
* [Interfaces](UIKit/Interfaces.md)

### Views

* [UIView](UIKit/UIView.md)
* [UIButton](UIKit/UIButton.md)
* [UIImageView](UIKit/UIImageView.md)
* [UILabel](UIKit/UILabel.md)
* [UITextField](UIKit/UITextField.md)
* [UITextView](UIKit/UITextView.md)
* [UICollectionView & UICollectionViewLayout & UICollectionViewCell](UIKit/UICollectionView.md)
* [UITableView & UITableViewCell](UIKit/UITableView.md)
* [UIScrollView](UIKit/UIScrollView.md)
* [UIRefreshControl](UIKit/UIRefreshControl.md)
* [UIFetchMoreControl](UIKit/UIFetchMoreControl.md)
* [UIAlert & UIPrompt & UIConfirm](UIKit/UIDialogs.md)
* [UIActivityIndicatorView](UIKit/UIActivityIndicatorView.md)
* [UISwitch](UIKit/UISwitch.md)
* [UISlider](UIKit/UISlider.md)
* [UIProgressView](UIKit/UIProgressView.md)
* [UIWebView](UIKit/UIWebView.md)
* [UIStackView](UIKit/UIStackView.md)

### View Controllers

* [UIViewController](UIKit/UIViewController.md)
* [UINavigationBarViewController](UIKit/UINavigationBarViewController.md)
* [UINavigationController](UIKit/UINavigationController.md)
* [UINavigationBar](UIKit/UINavigationBar.md)
* [UINavigationItem](UIKit/UINavigationItem.md)
* [UIBarButtonItem](UIKit/UIBarButtonItem.md)
* [UITabBarController](UIKit/UITabBarController.md)
* [UITabBar](UIKit/UITabBar.md)
* [UITabBarItem](UIKit/UITabBarItem.md)
* [UIPageViewControlller](UIKit/UIPageViewControlller.md)

### Other Classes

* [UIAnimator](UIKit/UIAnimator.md)
* [UIGestureRecognizer](UIKit/UIGestureRecognizer.md)
* [UIColor](UIKit/UIColor.md)
* [UIFont](UIKit/UIFont.md)
* [UIImage](UIKit/UIImage.md)
* [UIAttributedString](UIKit/UIAttributedString.md)
* [UIIndexPath](UIKit/UIIndexPath.md)
* [UIScreen](UIKit/UIScreen.md)
* [UIDevice](UIKit/UIDevice.md)
* [UIBezierPath](UIKit/UIBezierPath.md)

## CoreGraphics

2D Rendering system.

* [CALayer](CoreGraphics/CALayer.md)
* [CAGradientLayer](CoreGraphics/CAGradientLayer.md)
* [CAShapeLayer](CoreGraphics/CAShapeLayer.md)
* [CADisplayLink](CoreGraphics/CADisplayLink.md)
