# Foundation | URLRequest

A URL load request that is independent of protocol or URL scheme.

## URLRequest

```typescript

/**
 * Creates a URL request with the specified URL, cache policy, and timeout values.
 */
constructor(aURL: URL | string, cachePolicy?: URLRequestCachePolicy, timeout?: number)

/**
 * The HTTP request method.
 */
readonly HTTPMethod: string | undefined

/**
 * The URL being requested.
 */
readonly URL: URL

/**
 * All of the request’s HTTP header fields.
 */
readonly allHTTPHeaderFields: {[key: string]: any} | undefined

/**
 * Returns the value of the specified HTTP header field.
 */
valueForHTTPHeaderField(field: string): any | undefined

/**
 * The request body.
 */
readonly HTTPBody: Data | undefined

/**
 * Returns a mutable request.
 */
mutable(): MutableURLRequest

```

## MutableURLRequest extends URLRequest

```typescript

/**
 * Creates a mutable URL request with the specified URL, cache policy, and timeout values.
 */
constructor(aURL: URL | string, cachePolicy?: URLRequestCachePolicy, timeout?: number)

/**
 * The HTTP request method.
 */
HTTPMethod: string | undefined

/**
 * All of the request’s HTTP header fields.
 */
allHTTPHeaderFields: {[key: string]: any} | undefined

/**
 * Sets the specified HTTP header field.
 */
setValueForHTTPHeaderField(value: string, field: string): void

/**
 * The request body.
 */
HTTPBody: Data | undefined

/**
 * Returns an immutable request.
 */
immutable(): URLRequest

```


## URLRequestCachePolicy

```typescript

enum URLRequestCachePolicy {

    /**
     * Use the caching logic defined in the protocol implementation, if any, for a particular URL load request.
     */
    useProtocol,

    /**
     * The URL load should be loaded only from the originating source.
     */
    ignoringLocalCache,

    /**
     * Use existing cache data, regardless or age or expiration date, loading from originating source only if there is no cached data.
     */
    returnCacheElseLoad,

    /**
     * Use existing cache data, regardless or age or expiration date, and fail if no cached data is available.
     */
    returnCacheDontLoad,
}

```
