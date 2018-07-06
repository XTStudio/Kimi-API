# Foundation | UUID

A universally unique value that can be used to identify types, interfaces, and other items.

```typescript

/**
 * Initializes a new UUID with RFC 4122 version 4 random bytes.
 * Providing UUIDString will prevent random action.
 */
constructor(UUIDString?: string)

/**
 * The UUID as a string.
 */
readonly UUIDString: string

```