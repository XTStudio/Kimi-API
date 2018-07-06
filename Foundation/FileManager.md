# Foundation | FileManager

An object that provides a convenient interface to the contents of the file system.

```typescript

/**
 * Returns the shared file manager object for the process.
 */
static readonly defaultManager: FileManager

/**
 * Returns the document directory for the current application.
 */
readonly readonly documentDirectory: string

/**
 * Returns the library directory for the current application.
 */
readonly readonly libraryDirectory: string

/**
 * Returns the cache directory for the current application.
 */
readonly readonly cacheDirectory: string

/**
 * Returns the temporary directory for the current application.
 */
readonly readonly temporaryDirectory: string

/**
 * Returns an array of strings identifying the paths for all items in the specified directory.
 * If deepSearch as true, performs a deep enumeration of the specified directory and returns the paths of all of the contained subdirectories.
 */
subpathsAtPath(atPath: string, deepSearch?: boolean = false): string[]

/**
 * Creates a directory with given attributes at the specified path.
 */
createDirectory(atPath: string, withIntermediateDirectories: boolean): Error | undefined

/**
 * Creates a file with the specified content and attributes at the given location.
 */
createFile(atPath: string, data: Data): Error | undefined

/**
 * Returns the contents of the file at the specified path.
 */
readFile(atPath: string): Data | undefined

/**
 * Removes the file or directory at the specified path.
 */
removeItem(atPath: string): Error | undefined

/**
 * Copies the item at the specified path to a new location synchronously.
 */
copyItem(atPath: string, toPath: string): Error | undefined

/**
 * Moves the file or directory at the specified path to a new location synchronously.
 */
moveItem(atPath: string, toPath: string): Error | undefined

/**
 * Returns a Boolean value that indicates whether a file exists at a specified path.
 */
fileExists(atPath: string): boolean

/**
 * Returns a Boolean value that indicates whether a directory exists at a specified path.
 */
dirExists(atPath: string): boolean

```