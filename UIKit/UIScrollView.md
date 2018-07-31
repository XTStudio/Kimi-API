# UIKit | UIScrollView extends UIView

A view that allows the scrolling and zooming of its contained views.

```typescript
/**
 * The point at which the origin of the content view is offset from the origin of the scroll view.
 */
contentOffset: Point

/**
 * The size of the content view.
 */
contentSize: Size

/**
 * The custom distance that the content view is inset from the safe area or scroll view edges.
 */
contentInset: EdgeInset

/**
 * A Boolean value that determines whether scrolling is disabled in a particular direction.
 */
directionalLockEnabled: boolean

/**
 * A Boolean value that controls whether the scroll view bounces past the edge of content and back again.
 */
bounces: boolean

/**
 * A Boolean value that determines whether bouncing always occurs when vertical scrolling reaches the end of the content.
 */
alwaysBounceVertical: boolean

/**
 * A Boolean value that determines whether bouncing always occurs when horizontal scrolling reaches the end of the content view.
 */
alwaysBounceHorizontal: boolean

/**
 * A Boolean value that determines whether paging is enabled for the scroll view.
 */
pagingEnabled: boolean

/**
 * A Boolean value that determines whether scrolling is enabled.
 */
scrollEnabled: boolean

/**
 * A Boolean value that controls whether the horizontal scroll indicator is visible.
 */
showsHorizontalScrollIndicator: boolean

/**
 * A Boolean value that controls whether the vertical scroll indicator is visible.
 */
showsVerticalScrollIndicator: boolean

/**
 * Sets the offset from the content view’s origin that corresponds to the receiver’s origin.
 */
setContentOffset(contentOffset: Point, animated: boolean): void

/**
 * Scrolls a specific area of the content so that it is visible in the receiver.
 */
scrollRectToVisible(rect: Rect, animated: boolean): void

/**
 * Returns whether the user has touched the content to initiate scrolling.
 */
readonly tracking: boolean

/**
 * A Boolean value that indicates whether the user has begun scrolling the content.
 */
readonly dragging: boolean

/**
 * Returns whether the content is moving in the scroll view after the user lifted their finger.
 */
readonly decelerating: boolean

/**
 * A Boolean value that controls whether the scroll-to-top gesture is enabled.
 */
scrollsToTop: boolean

/**
 * Tells when the user scrolls the content view within the receiver.
 */
on('didScroll', (sender: UIScrollView) => void): this

/**
 * Tells when the scroll view is about to start scrolling the content.
 */
on('willBeginDragging', (sender: UIScrollView) => void): this

/**
 * Tells when the user finishes scrolling the content.
 * Returns target animation end contentOffset optionally.
 */
on('willEndDragging', (sender: UIScrollView, velocity: Point) => Point | undefined): this

/**
 * Tells when dragging ended in the scroll view.
 */
on('didEndDragging', (sender: UIScrollView, decelerate: boolean) => void): this

/**
 * Tells that the scroll view is starting to decelerate the scrolling movement.
 */
on('willBeginDecelerating', (sender: UIScrollView) => void): this

/**
 * Tells that the scroll view is ends to decelerate the scrolling movement.
 */
on('didEndDecelerating', (sender: UIScrollView) => void): this

/**
 * Tells that the scroll view has ended decelerating the scrolling movement.
 */
on('didEndScrollingAnimation', (sender: UIScrollView) => void): this

/**
 * Tells that the scroll view scrolled to the top of the content.
 */
on('didScrollToTop', (sender: UIScrollView) => void): this
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uiscrollviewdelegate?language=objc)
* [Point / Size / EdgeInset / Rect](Interfaces.md)