# UIKit | UIStackView extends UIView

A streamlined interface for laying out a collection of views in either a column or a row.

```typescript

/**
 * Returns a new stack view object that manages the provided views.
 */
constructor(arrangedSubviews: UIView[])

/**
 * The list of views arranged by the stack view.
 */
readonly arrangedSubviews: UIView[]

/**
 * Adds a view to the end of the arrangedSubviews array.
 */
addArrangedSubview(view: UIView): void

/**
 * Removes the provided view from the stack’s array of arranged subviews.
 */
removeArrangedSubview(view: UIView): void

/**
 * Adds the provided view to the array of arranged subviews at the specified index.
 */
insertArrangedSubview(view: UIView, atIndex: number): void

/**
 * Specific an arranged subview's size.
 */
layoutArrangedSubview(subview: UIView, size: {width?: number, height?: number}): void

/**
 * The axis along which the arranged views are laid out.
 */
axis: UILayoutConstraintAxis

/**
 * The distribution of the arranged views along the stack view’s axis.
 */
distribution: UIStackViewDistribution

/**
 * The alignment of the arranged subviews perpendicular to the stack view’s axis.
 */
alignment: UIStackViewAlignment

/**
 * The distance in points between the adjacent edges of the stack view’s arranged views.
 */
spacing: number

```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uistackview?language=objc)
* [UILayoutConstraintAxis / UIStackViewDistribution / UIStackViewAlignment](Enums.md)