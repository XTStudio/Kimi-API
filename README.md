# Kimi-API

Kimi is a framework exposes iOS / Android / Web features.

Kimi including following framework subsets now.

* Foundation
* UIKit
* CoreGraphics

## Definitions

All defines as TypeScript typings excepts followings.

### kill null 

Will NEVER deliver and receive ```null``` object.

### ? means optional

eg ```superview: UIView?``` means superview property may return ```undefined``` result.

eg ```willMoveToSuperview(superview: UIView?)``` means superview maybe ```undefined```.

### Structs

Structs means interface.

## Foundation

You use Foundation framework manage I/O things, such as Networking / File / Data jobs.

## UIKit

You use UIKit framework to display User Interface on device.

### Structs

```
Rect = {x: number, y: number, width: number, height: number}
Point = {x: number, y: number}
AffineTransform = {a: number, b: number, c: number, d: number, tx: number, ty: number}
```

### UIView

```
// Boxing
frame: Rect
bounds: Rect
center: Point
transform: AffineTransform

// Actions
superview: UIView?
subviews: UIView[]
removeFromSuperview(): void
insertSubviewAtIndex(view: UIView, index: number): void
exchangeSubview(index1: number, index2: number): void
addSubview(view: UIView): void
insertSubviewBelowSubview(view: UIView, belowSubview: UIView): void
insertSubviewAboveSubview(view: UIView, aboveSubview: UIView): void
bringSubviewToFront(view: UIView): void
sendSubviewToBack(view: UIView): void
isDescendantOfView(view: UIView): boolean
viewWithTag(tag: number): UIView?

// Delegates
didAddSubview(subview: UIView): void
willRemoveSubview(subview: UIView): void
willMoveToSuperview(newSuperview: UIView): void
didMoveToSuperview(): void
setNeedsLayout(): void
layoutIfNeeded(): void
layoutSubviews(): void

// Rendering
setNeedsDisplay(): void
clipsToBounds: boolean
backgroundColor: UIColor?
alpha: number
hidden: boolean
contentMode: number
tintColor: UIColor
tintColorDidChange(): void
```

### UIColor

## CoreGraphics

