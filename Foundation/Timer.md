# Foundation | Timer

A timer that fires after a certain time interval has elapsed, sending a specified message to a target object.

```typescript

/**
 * Creates a timer and schedules it on the current run loop in the default mode, you may set it repeats or not.
 */
constructor(timeInterval: number, block: () => void, repeats: boolean)

/**
 * A Boolean value that indicates whether the timer is currently valid.
 */
readonly valid: boolean

/**
 * Causes the timer's message to be sent to its block.
 */
fire(): void

/**
 * Stops the timer from ever firing again and requests its removal from its run loop.
 */
invalidate(): void

```