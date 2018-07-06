# Foundation | URLResponse

The metadata associated with the response to a URL load request, independent of protocol and URL scheme.

```typescript

/**
 * The URL for the response.
 */
readonly URL: URL | undefined

/**
 * The expected length of the response’s content.
 */
readonly expectedContentLength: number

/**
 * The MIME type of the response.
 */
readonly MIMEType: string | undefined

/**
 * The name of the text encoding provided by the response’s originating source.
 */
readonly textEncodingName: string | undefined

/**
 * The HTTP status code of the receiver. 
 */
readonly statusCode: number

/**
 * A dictionary containing all the HTTP header fields of the receiver.
 */
readonly allHeaderFields: {[key: string]: any}

```