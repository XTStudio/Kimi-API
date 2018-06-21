# Kimi-API

Kimi is a framework exposes iOS / Android / Web features.

Kimi including following framework subsets now.

* Foundation
* UIKit
* CoreGraphics

## EventEmitter

All objects extends [EventEmitter](https://github.com/Olical/EventEmitter), that means you could listen via EventEmitter, and emit event to objects.

## NO Null

Kimi will not accept null as argument and return value, optional value will be ```undefined```.

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

### Interface

```typescript
Rect = {x: number, y: number, width: number, height: number}
Point = {x: number, y: number}
AffineTransform = {a: number, b: number, c: number, d: number, tx: number, ty: number}
EdgeInsets = {top: number, left: number, bottom: number, right: number}
```

### UIView

```typescript

// Constructors
constructor(): UIView
readonly layer: CALayer

// Geometry
frame: Rect
bounds: Rect
center: Point
transform: AffineTransform

// Hierarchy
tag: number = 0
readonly superview: UIView?
readonly subviews: UIView[]
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
readonly state: UIGestureRecognizerState
enabled: boolean
readonly view: UIView?
requiresExclusiveTouchType: boolean
requireGestureRecognizerToFail(otherGestureRecognizer: UIGestureRecognizer): void
locationInView(view: UIView): Point
```

### UIGestureRecognizerState

```typescript
enum UIGestureRecognizerState {
  possible
  began
  changed
  ended
  cancelled
  failed
}
```

### UITapGestureRecognizer: UIGestureRecognizer

```typescript

numberOfTapsRequired: number = 1
numberOfTouchesRequired: number = 1
on('touch', (sender: UITapGestureRecognizer) => void): void
```

### UILongPressGestureRecognizer: UIGestureRecognizer

```typescript
numberOfTapsRequired: number = 0
numberOfTouchesRequired: number = 1
minimumPressDuration: number = 0.5
allowableMovement: number = 10
on('began', (sender: UILongPressGestureRecognizer) => void): void
on('changed', (sender: UILongPressGestureRecognizer) => void): void
on('ended', (sender: UILongPressGestureRecognizer) => void): void
on('cancelled', (sender: UILongPressGestureRecognizer) => void): void
```

### UIPanGestureRecognizer: UIGestureRecognizer

```typescript
minimumNumberOfTouches: number = 1
maximumNumberOfTouches: number = Infinite
translationInView:(view: UIView?): Point
setTranslation:(translate: Point, inView: UIView?): void
velocityInView:(view: UIView?): Point
on('began', (sender: UIPanGestureRecognizer) => void): void
on('changed', (sender: UIPanGestureRecognizer) => void): void
on('ended', (sender: UIPanGestureRecognizer) => void): void
on('cancelled', (sender: UIPanGestureRecognizer) => void): void
```

### UIPinchGestureRecognizer: UIGestureRecognizer

```typescript
scale: number
readonly velocity: number
on('began', (sender: UIPinchGestureRecognizer) => void): void
on('changed', (sender: UIPinchGestureRecognizer) => void): void
on('ended', (sender: UIPinchGestureRecognizer) => void): void
on('cancelled', (sender: UIPinchGestureRecognizer) => void): void
```

### UIRotationGestureRecognizer: UIGestureRecognizer

```typescript
rotation: number
readonly velocity: number
on('began', (sender: UIRotationGestureRecognizer) => void): void
on('changed', (sender: UIRotationGestureRecognizer) => void): void
on('ended', (sender: UIRotationGestureRecognizer) => void): void
on('cancelled', (sender: UIRotationGestureRecognizer) => void): void
```

### UIColor

```typescript
constructor(r: number, g: number, b: number, a: number): UIColor
```

### UIButton: UIView

```typescript
constructor(isCustom: boolean? = false)
enabled: boolean
selected: boolean
readonly highlighted: boolean
readonly tracking: boolean
readonly touchInside: boolean
contentVerticalAlignment: UIControlContentVerticalAlignment
contentHorizontalAlignment: UIControlContentHorizontalAlignment
setTitle(title?: string, state: UIControlState): void
setTitleColor(color?: UIColor, state: UIControlState): void
setTitleFont(font: UIFont): void
setImage(image?: UIImage, state: UIControlState): void
contentEdgeInsets: EdgeInsets
titleEdgeInsets: EdgeInsets
imageEdgeInsets: EdgeInsets
on('touchDown', (sender: UIButton) => void): void
on('touchDownRepeat', (sender: UIButton) => void): void
on('touchDragInside', (sender: UIButton) => void): void
on('touchDragOutside', (sender: UIButton) => void): void
on('touchDragEnter', (sender: UIButton) => void): void
on('touchDragExit', (sender: UIButton) => void): void
on('touchUpInside', (sender: UIButton) => void): void
on('touchUpOutside', (sender: UIButton) => void): void
on('touchCancel', (sender: UIButton) => void): void
```

### UIControlState

```typescript
enum options UIControlState {
  normal,
  highlighted,
  disabled,
  selected,
}
```

### UIControlContentVerticalAlignment

```typescript
enum UIControlContentVerticalAlignment {
  center,
  top,
  bottom,
  fill,
}
```

### UIControlContentHorizontalAlignment

```typescript
enum UIControlContentVerticalAlignment {
  center,
  left,
  right,
  fill,
}
```

### UIFont

```typescript
constructor(pointSize: number, 
            fontStyle?: "thin" | "light" | "regular" | "medium" | "bold" | "heavy" | "black" | "italic",
            fontName?: string)
```

## CoreGraphics

### CALayer

```typescript
// Geometry
frame: Rect
// Hierarchy
readonly superlayer: CALayer?
removeFromSuperlayer(): void
readonly sublayers: CALayer[]
addSublayer(layer: CALayer): void
insertSublayerAtIndex(layer: CALayer, index: number): void
insertSublayerBelow(layer: CALayer, below: CALayer): void
insertSublayerAbove(layer: CALayer, above: CALayer): void
replaceSublayer(layer: CALayer, layer2: CALayer): void
// Rendering
hidden: boolean
mask: CALayer?
masksToBounds: boolean
backgroundColor: UIColor?
cornerRadius: number
borderWidth: number
borderColor: UIColor?
opacity: number
shadowColor: UIColor?
shadowOpacity: number
shadowOffset: Size
shadowRadius: number
```

