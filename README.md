# Kimi-API

Kimi is a framework exposes iOS / Android / Web features.

Kimi including following framework subsets now.

* Foundation
* UIKit
* CoreGraphics

## EventEmitter

All objects extends [EventEmitter](https://github.com/Olical/EventEmitter), that means you could listen via EventEmitter, and emit event to objects.

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

### DispatchQueue

You use ```DispatchQueue``` as timer, async task creater, etc.

```typescript

static main: DispatchQueue
constructor(identifier: string?): DispatchQueue
async(asyncBlock: () => void): void
asyncAfter(delayInSeconds: number, asyncBlock: () => void): void

```

## UIKit

You use UIKit framework to display User Interface on device.

### Structs

```typescript
Rect = {x: number, y: number, width: number, height: number}
Point = {x: number, y: number}
AffineTransform = {a: number, b: number, c: number, d: number, tx: number, ty: number}
```

### UIView

```typescript

// Constructors
constructor(): UIView

// Geometry
frame: Rect
bounds: Rect
center: Point
transform: AffineTransform

// Hierarchy
tag: number = 0
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

// GestureRecognizers
userInteractionEnabled: boolean
gestureRecognizers: UIGestureRecognizer[]
addGestureRecognizer(gestureRecognizer: UIGestureRecognizer): void
removeGestureRecognizer(gestureRecognizer: UIGestureRecognizer): void

```

### UIAnimator

```typescript
static shared: UIAnimator
linear(duration: number, animations: () => void, completion?: (finished: boolean) => void): void
spring(tension: number, friction: number, animations: () => void, completion?: () => void): void
```

### UIGestureRecognizer

```typescript
state: UIGestureRecognizerState
enabled: boolean
view: UIView?
requiresExclusiveTouchType: boolean
requireGestureRecognizerToFail(otherGestureRecognizer: UIGestureRecognizer): void
locationInView(view: UIView): Point
```

### UIGestureRecognizerState

```typescript
enum {
  Possible
  Began
  Changed
  Ended
  Cancelled
  Failed
}
```

### UITapGestureRecognizer: UIGestureRecognizer

```typescript

numberOfTapsRequired: number = 1
numberOfTouchesRequired: number = 1
on('touch', () => void): void
```

### UIColor

```typescript
constructor(r: number, g: number, b: number, a: number): UIColor
```

## CoreGraphics

