# UIKit | UIImage


## UIImageRenderingMode

Specifies the possible rendering modes for an image.

```typescript
enum UIImageRenderingMode {
    /**
     * Use the default rendering mode for the context where the image is used. 
     */
    automatic

    /**
     * Always draw the original image, without treating it as a template.
     */
    alwaysOriginal

    /**
     * Always draw the image as a template image, ignoring its color information.
     */
    alwaysTemplate
}
```

## UIImage

An object that manages image data in your app.

```typescript

/**
 * name - The application bundle assets name.
 * base64 - Use a base64 string to decode image.
 * renderingMode - Specifies the possible rendering modes for an image.
 */
constructor({name?: string, base64?: string, data?: Data, renderingMode?: UIImageRenderingMode})

/**
 * The logical dimensions of the image, measured in points.
 */
readonly size: Size

/**
 * The scale factor of the image.
 */
readonly scale: number

/**
 * Call after image loaded, only valid on Web Platform.
 */
on('load', () => void): this
```