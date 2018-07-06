# Foundation | URL

An object that represents the location of a resource, such as an item on a remote server or the path to a local file.

```typescript

/**
 * Creates and returns an URL object initialized with a base URL and a relative string.
 */
static URLWithString(string: string, baseURL?: URL): URL | undefined

/**
 * Initializes and returns a newly created URL object as a file URL with a specified path.
 */
static fileURLWithPath(path: string): URL | undefined

/**
 * The URL string for the receiver as an absolute URL. 
 */
readonly absoluteString: string

```