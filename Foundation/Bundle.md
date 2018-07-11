# Foundation | Bundle

A representation of the code and resources stored in a bundle directory on disk.

```typescript

/**
 * Returns the bundle of native application.
 */
static readonly native: Bundle

/**
 * Returns the bundle of JavaScript application.
 */
static readonly js: Bundle

/**
 * Returns a specific file path in bundle.
 */
resourcePath(name: string, type?: string, inDirectory?: string): string | undefined

/**
 * Returns a specific file url in bundle.
 */
resourceURL(name: string, type?: string, inDirectory?: string): URL | undefined

```
