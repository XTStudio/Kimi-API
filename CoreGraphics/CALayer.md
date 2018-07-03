# CoreGraphics > CALayer

An object that manages image-based content and allows you to perform animations on that content.

```typescript
/**
 * The layer’s frame rectangle.
 */
frame: Rect

/**
 * The superlayer of the layer.
 */
readonly superlayer: CALayer | undefined

/**
 * Detaches the layer from its parent layer.
 */
removeFromSuperlayer(): void

/**
 * An array containing the layer’s sublayers.
 */
readonly sublayers: CALayer[]

/**
 * An array containing the layer’s sublayers.
 */
addSublayer(layer: CALayer): void

/**
 * Inserts the specified layer into the receiver’s list of sublayers at the specified index.
 */
insertSublayerAtIndex(layer: CALayer, index: number): void

/**
 * Inserts the specified sublayer below a different sublayer that already belongs to the receiver.
 */
insertSublayerBelow(layer: CALayer, below: CALayer): void

/**
 * Inserts the specified sublayer above a different sublayer that already belongs to the receiver.
 */
insertSublayerAbove(layer: CALayer, above: CALayer): void

/**
 * Replaces the specified sublayer with a different layer object.
 */
replaceSublayer(layer: CALayer, layer2: CALayer): void

/**
 * A Boolean indicating whether the layer is displayed. Animatable.
 */
hidden: boolean

/**
 * An optional layer whose alpha channel is used to mask the layer’s content.
 */
mask: CALayer | undefined

/**
 * A Boolean indicating whether sublayers are clipped to the layer’s bounds. Animatable.
 */
masksToBounds: boolean

/**
 * The background color of the receiver. Animatable.
 */
backgroundColor: UIColor | undefined

/**
 * The radius to use when drawing rounded corners for the layer’s background. Animatable.
 */
cornerRadius: number

/**
 * The width of the layer’s border. Animatable.
 */
borderWidth: number

/**
 * The color of the layer’s border. Animatable.
 */
borderColor: UIColor | undefined

/**
 * The opacity of the receiver. Animatable.
 */
opacity: number

/**
 * The color of the layer’s shadow. Animatable.
 */
shadowColor: UIColor | undefined

/**
 * The opacity of the layer’s shadow. Animatable.
 */
shadowOpacity: number

/**
 * The offset (in points) of the layer’s shadow. Animatable.
 */
shadowOffset: Size

/**
 * The blur radius (in points) used to render the layer’s shadow. Animatable.
 */
shadowRadius: number
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/quartzcore/calayer?language=objc)
* [UIColor](../UIKit/UIColor.md)
* [Rect / Size](../UIKit/Interfaces.md)