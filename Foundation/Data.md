# Foundation | Data

## Data

A static byte buffer in memory.

```typescript

/**
 * Creates and returns a data object, using the one of following parameter will create an object with specific binary data.
 */
constructor(value?: ArrayBuffer | {
                                     utf8String?: string, 
                                     base64EncodedData?: Data,
                                     base64EncodedString?: string,
                                  })

/**
 * Returns an array-buffer object.
 */
arrayBuffer(): ArrayBuffer

/**
 * Returns a json object, otherwise returns undefined if it's not an utf8 string encoding data or parse error.
 */
json(): any | undefined

/**
 * Returns an utf8 string, undefined if it's not an utf8 string encoding data.
 */
utf8String(): string | undefined

/**
 * Creates a Base64, UTF-8 encoded data object from the string.
 */
base64EncodedData(): Data

/**
 * Creates a Base64 encoded string from the string.
 */
base64EncodedString(): string

/**
 * Returns a mutable data object.
 */
mutable(): MutableData

```

## MutableData extends Data

```typescript

/**
 * Creates and returns a mutable data object, using the one of following parameter will create an object with specific binary data.
 */
constructor(value?: ArrayBuffer | {
                                     utf8String?: string, 
                                     base64EncodedData?: Data,
                                     base64EncodedString?: string,
                                  })

/**
 * Appends the content of another data object to the receiver.
 */
appendData(data: Data): void

/**
 * Appends the content of another array-buffer to the receiver.
 */
appendArrayBuffer(arrayBuffer: ArrayBuffer): void

/**
 * Replaces the entire contents of the receiver with the contents of another data object.
 */
setData(data: Data): void

/**
 * Returns an immutable data object.
 */
immutable(): Data

```
