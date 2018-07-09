# Foundation | UserDefaults

An interface to the user’s defaults database, where you store key-value pairs persistently across launches of your app.

```typescript

/**
 * Returns the shared defaults object.
 */
static readonly standard: UserDefaults

/**
 * Creates a user defaults object initialized with the defaults for the specified database name.
 */
constructor(suiteName?: string)

/**
 * Returns the object associated with the specified key.
 */
valueForKey(forKey: string): any | undefined

/**
 * Sets the value of the specified default key.
 */
setValue(value: any, forKey: string): void

/**
 * Reset all values.
 */
reset(): void

```
