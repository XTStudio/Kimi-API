# CoreGraphics | CADisplayLink

A timer object that allows your application to synchronize its drawing to the refresh rate of the display.

```typescript

/**
 * Returns a new display link.
 */
constructor(vsyncBlock: () => void)

/**
 * The time value associated with the last frame that was displayed.
 */
timestamp: number

/**
 * Registers the display link with a run loop.
 */
active(): void

/**
 * Removes the display link from all run loop modes.
 */
invalidate(): void

```