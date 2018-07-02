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
constructor(identifier?: string): DispatchQueue
async(asyncBlock: () => void): void
asyncAfter(delayInSeconds: number, asyncBlock: () => void): void

```

## UIKit

You use UIKit framework to display User Interface on device.

### Interface

```typescript
Rect = {x: number, y: number, width: number, height: number}
Point = {x: number, y: number}
Size = {width: number, height: number}
AffineTransform = {a: number, b: number, c: number, d: number, tx: number, ty: number}
EdgeInsets = {top: number, left: number, bottom: number, right: number}
Range = {location: number, length: number}
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
readonly superview: UIView | undefined
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
viewWithTag(tag: number): UIView | undefined

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
backgroundColor: UIColor | undefined
alpha: number
hidden: boolean
contentMode: UIViewContentMode
tintColor: UIColor
tintColorDidChange(): void

// GestureRecognizers
userInteractionEnabled: boolean
gestureRecognizers: UIGestureRecognizer[]
addGestureRecognizer(gestureRecognizer: UIGestureRecognizer): void
removeGestureRecognizer(gestureRecognizer: UIGestureRecognizer): void

```

### UIViewContentMode

```typescript
enum UIViewContentMode {
  scaleToFill
  scaleAspectFit
  scaleAspectFill
}
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
readonly view: UIView | undefined
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
translationInView:(view?: UIView): Point
setTranslation:(translate: Point, inView?: UIView): void
velocityInView:(view?: UIView): Point
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
constructor(isCustom?: boolean = false)
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

### UIImageView: UIView

```typescript
image?: UIImage
```

### UIImage

```typescript
constructor({name?: string, base64?: string, renderingMode?: UIImageRenderingMode})
readonly size: Size
readonly scale: number
```

### UIImageRenderingMode

```typescript
enum UIImageRenderingMode {
  automatic
  alwaysOriginal
  alwaysTemplate
}
```

### UILabel: UIView

```typescript
text: string | undefined
attributedText: UIAttributedString | undefined
font: UIFont | undefined
textColor: UIColor | undefined
textAlignment: UITextAlignment
lineBreakMode: UILineBreakMode
numberOfLines: number
```

### UIAttributedString

```typescript
constructor(str: string, attributes: {[key: string]: any})  // attributes -> key: UIAttributedStringKey
mutable(): UIMutableAttributedString
```

### UIMutableAttributedString: UIAttributedString

```typescript
constructor(str: string, attributes: {[key: string]: any})  // attributes -> key: UIAttributedStringKey
replaceCharacters(inRange: Range, withString: string): void
setAttributes(attributes: {[key: string]: any}, range: Range): void
addAttribute(attrName: string, value: any, range: Range): void
addAttributes(attributes: {[key: string]: any}, range: Range): void
removeAttribute(attrName: string, range: Range): void
replaceCharactersWithAttributedString(inRange: Range, withAttributedString: UIAttributedString): void
insertAttributedString(attributedString: UIAttributedString, atIndex: number): void
appendAttributedString(attributedString: UIAttributedString): void
deleteCharacters(inRange: Range): void
immutable(): UIAttributedString
```

### UIAttributedStringKey

```typescript
const UIForegroundColorAttributeName: string      // value: UIColor
const UIFontAttributeName: string                 // value: UIFont
const UIBackgroundColorAttributeName: string      // value: UIColor
const UIKernAttributeName: string                 // value: number
const UIStrikethroughStyleAttributeName: string   // value: number
const UIUnderlineStyleAttributeName: string       // value: number
const UIStrokeColorAttributeName: string          // value: UIColor
const UIStrokeWidthAttributeName: string          // value: number
const UIUnderlineColorAttributeName: string       // value: UIColor
const UIStrikethroughColorAttributeName: string   // value: UIColor
```

### UITextAlignment

```typescript
enum UITextAlignment {
  left
  center
  right
}
```

### UILineBreakMode

```typescript
enum UILineBreakMode {
  wordWrapping
  charWrapping
  clipping
  truncatingHead
  truncatingTail
  truncatingMiddle
}
```

### UITextField: UIView

```typescript
// TextField
text: string | undefined
textColor: UIColor | undefined
font: UIFont | undefined
textAlignment: UITextAlignment
placeholder: string | undefined
clearsOnBeginEditing: boolean
readonly editing: boolean
clearButtonMode: UITextFieldViewMode
leftView: UIView | undefined
leftViewMode: UITextFieldViewMode
rightView: UIView | undefined
rightViewMode: UITextFieldViewMode
clearsOnInsertion: boolean 
focus(): void
blur(): void
// TextInputTraits
autocapitalizationType: UITextAutocapitalizationType
autocorrectionType: UITextAutocorrectionType
spellCheckingType: UITextSpellCheckingType
keyboardType: UIKeyboardType
returnKeyType: UIReturnKeyType
secureTextEntry: boolean
// Callbacks
on('shouldBeginEditing', (sender: UITextField) => boolean): void
on('didBeginEditing', (sender: UITextField) => void): void
on('shouldEndEditing', (sender: UITextField) => boolean): void
on('didEndEditing', (sender: UITextField) => void): void
on('shouldChange', (sender: UITextField, charactersInRange: Range, replacementString: string) => boolean): void
on('shouldClear', (sender: UITextField) => boolean): void
on('shouldReturn', (sender: UITextField) => boolean): void
```

### UITextView: UIScrollView

```typescript
// TextView
text: string | undefined
textColor: UIColor | undefined
font: UIFont | undefined
textAlignment: UITextAlignment
editable: boolean
selectable: boolean
readonly editing: boolean
scrollRangeToVisible(range: Range): void
focus(): void
blur(): void
// TextInputTraits
autocapitalizationType: UITextAutocapitalizationType
autocorrectionType: UITextAutocorrectionType
spellCheckingType: UITextSpellCheckingType
keyboardType: UIKeyboardType
returnKeyType: UIReturnKeyType
secureTextEntry: boolean
// Callbacks
on('shouldBeginEditing', (sender: UITextView) => boolean): void
on('didBeginEditing', (sender: UITextView) => void): void
on('shouldEndEditing', (sender: UITextView) => boolean): void
on('didEndEditing', (sender: UITextView) => void): void
on('shouldChange', (sender: UITextView, charactersInRange: Range, replacementString: string) => boolean): void
```

### UITextFieldViewMode

```typescript
enum UITextFieldViewMode {
  never
  whileEditing
  unlessEditing
  always
}
```

### UITextAutocapitalizationType

```typescript
enum UITextAutocapitalizationType {
  none,
  words,
  sentences,
  allCharacters,
}
```

### UITextAutocorrectionType

```typescript
enum UITextAutocorrectionType {
  default,
  no,
  yes,
}
```

### UITextSpellCheckingType

```typescript
enum UITextSpellCheckingType {
  default,
  no,
  yes
}
```

### UIKeyboardType

```typescript
enum UIKeyboardType {
  default,
  ASCIICapable
  numbersAndPunctuation,
  numberPad,
  phonePad,
  emailAddress,
  decimalPad
}
```

### UIReturnKeyType

```typescript
enum UIReturnKeyType {
  default,
  go,
  next,
  send,
  done
}
```

### UIScrollView: UIView

```typescript
contentOffset: Point
contentSize: Size
contentInset: EdgeInset
directionalLockEnabled: boolean
bounces: boolean
alwaysBounceVertical: boolean
alwaysBounceHorizontal: boolean
pagingEnabled: boolean
scrollEnabled: boolean
showsHorizontalScrollIndicator: boolean
showsVerticalScrollIndicator: boolean
decelerationRate: number
setContentOffset(contentOffset: Point, animated: boolean): void
scrollRectToVisible(rect: Rect, animated: boolean): void
readonly tracking: boolean
readonly dragging: boolean
readonly decelerating: boolean
scrollsToTop: boolean
on('didScroll', (sender: UIScrollView) => void): void
on('willBeginDragging', (sender: UIScrollView) => void): void
on('willEndDragging', (sender: UIScrollView, velocity: Point) => Point | undefined): void
on('didEndDragging', (sender: UIScrollView, decelerate: boolean) => void): void
on('willBeginDecelerating', (sender: UIScrollView) => void): void
on('didEndScrollingAnimation', (sender: UIScrollView) => void): void
on('didScrollToTop', (sender: UIScrollView) => void): void
```

### UITableView: UIScrollView

```typescript
// Properties
tableHeaderView: UIView | undefined
tableFooterView: UIView | undefined
separatorColor: UIColor | undefined
separatorInset: EdgeInsets
allowsSelection: boolean
allowsMultipleSelection: boolean
// Methods
register(initializer: (context: any) => UITableViewCell, reuseIdentifier: string)
dequeueReusableCell(reuseIdentifier: string, indexPath: UIIndexPath): UITableViewCell
reloadData(): void
selectRow(indexPath: UIIndexPath, animated: boolean): void
deselectRow(indexPath: UIIndexPath, animated: boolean): void
// Delegates
on('numberOfSections', () => number): void
on('numberOfRows', (inSection: number) => number): void
on('heightForRow', (indexPath: UIIndexPath) => number): void
on('cellForRow', (indexPath: UIIndexPath) => UITableViewCell): void
on('viewForHeader', (inSection: number) => UIView | undefined): void
on('heightForHeader', (inSection: number) => number): void
on('viewForFooter', (inSection: number) => UIView | undefined): void
on('heightForFooter', (inSection: number) => number): void
on('didSelectRow', (indexPath: UIIndexPath, cell: UITableViewCell) => void): void
on('didDeselectRow', (indexPath: UIIndexPath, cell: UITableViewCell) => void): void
```

### UITableViewCell: UIView

```typescript
constructor(context: any)
readonly contentView: UIView
readonly reuseIdentifier: string | undefined
hasSelectionStyle: boolean = true
on('selected', (sender: UITableViewCell, selected: boolean, animated: boolean) => void): void
on('highlighted', (sender: UITableViewCell, highlighted: boolean, animated: boolean) => void): void
```

### UIIndexPath

```typescript
constructor(row: number, section: number)
readonly row: number
readonly section: number
```

### UICollectionView: UIScrollView

```typescript
constructor(collectionViewLayout: UICollectionViewLayout)
readonly collectionViewLayout: UICollectionViewLayout
allowsSelection: boolean
allowsMultipleSelection: boolean
// Methods
register(initializer: (context: any) => UICollectionViewCell, reuseIdentifier: string)
dequeueReusableCell(reuseIdentifier: string, indexPath: UIIndexPath): UICollectionViewCell
reloadData(): void
selectItem(indexPath: UIIndexPath, animated: boolean): void
deselectItem(indexPath: UIIndexPath, animated: boolean): void
// Delegates
on('numberOfSections', () => number): void
on('numberOfItems', (inSection: number) => number): void
on('cellForItem', (indexPath: UIIndexPath) => UICollectionViewCell): void
on('didSelectItem', (indexPath: UIIndexPath, cell: UICollectionViewCell) => void): void
on('didDeselectItem', (indexPath: UIIndexPath, cell: UICollectionViewCell) => void): void
```

### UICollectionViewCell: UIView

```typescript
constructor(context: any)
readonly contentView: UIView
readonly reuseIdentifier: string | undefined
on('selected', (sender: UITableViewCell, selected: boolean) => void): void
on('highlighted', (sender: UITableViewCell, highlighted: boolean) => void): void
```

### UICollectionViewLayout

```typescript
readonly collectionView: UICollectionView | undefined
invalidateLayout(): void
```

### UICollectionViewFlowLayout: UICollectionViewLayout

```typescript
minimumLineSpacing: number
minimumInteritemSpacing: number
itemSize: Size
headerReferenceSize: Size
footerReferenceSize: Size
sectionInset: EdgeInsets
scrollDirection: UICollectionViewScrollDirection = .vertical
on('sizeForItem', (indexPath: IndexPath) => Size): void
on('insetForSection', (inSection: number) => EdgeInsets): void
on('minimumLineSpacing', (inSection: number) => number): void
on('minimumInteritemSpacing', (inSection: number) => number): void
on('referenceSizeForHeader', (inSection: number) => Size): void
on('referenceSizeForFooter', (inSection: number) => Size): void
```

### UICollectionViewScrollDirection

```typescript
enum UICollectionViewScrollDirection {
  vertical,
  horizontal,
}
```

### UIAlert

```typescript
constructor(message: string, buttonText: string = "OK")
show(completed: () => void): void
```

### UIPrompt

```typescript
constructor(message: string)
confirmTitle: string = "Done"
cancelTitle: string = "Cancel"
placeholder: string
defaultValue: string
show(completed: (text: string) => void, cancelled?: () => void): void
```

### UIConfirm

```typescript
constructor(message: string)
confirmTitle: string = "Yes"
cancelTitle: string = "No"
show(completed?: () => void, cancelled?: () => void): void
```

### UIActivityIndicatorView: UIView

```typescript
color: UIColor
largeStyle: boolean
readonly animating: boolean
startAnimating(): void
stopAnimating(): void
```

### UISwitch: UIView

```typescript
onTintColor: UIColor | undefined
thumbTintColor: UIColor | undefined
isOn: boolean
setOn(on: boolean, animated: boolean): void
on('valueChanged', (sender: UISwitch) => void): void
```

### UISlider: UIView

```typescript
value: number = 0.0
minimumValue: number = 0.0
maximumValue: number = 1.0
minimumTrackTintColor: UIColor | undefined
maximumTrackTintColor: UIColor | undefined
thumbTintColor: UIColor | undefined
setValue(value: number, animated: boolean): void
on('valueChanged', (sender: UISlider) => void): void
```

### UIWebView: UIView

```typescript
// Properties
readonly title: string | undefined
readonly URL: NSURL | undefined
readonly loading: boolean
// Methods
loadRequest(request: NSURLRequest): void
loadHTMLString(HTMLString: string, baseURL: NSURL): void
goBack(): void
goForward(): void
reload(): void
stopLoading(): void
evaluateJavaScript(script: string, completed: (result?: any, error?: Error) => void): void
// Delegates
on('newRequest', (request: NSURLRequest) => boolean): void
on('didStart', () => void): void
on('didFinish', () => void): void
on('didFail', (error: Error) => void): void
```

## CoreGraphics

### CALayer

```typescript
// Geometry
frame: Rect
// Hierarchy
readonly superlayer: CALayer | undefined
removeFromSuperlayer(): void
readonly sublayers: CALayer[]
addSublayer(layer: CALayer): void
insertSublayerAtIndex(layer: CALayer, index: number): void
insertSublayerBelow(layer: CALayer, below: CALayer): void
insertSublayerAbove(layer: CALayer, above: CALayer): void
replaceSublayer(layer: CALayer, layer2: CALayer): void
// Rendering
hidden: boolean
mask: CALayer | undefined
masksToBounds: boolean
backgroundColor: UIColor | undefined
cornerRadius: number
borderWidth: number
borderColor: UIColor | undefined
opacity: number
shadowColor: UIColor | undefined
shadowOpacity: number
shadowOffset: Size
shadowRadius: number
```

