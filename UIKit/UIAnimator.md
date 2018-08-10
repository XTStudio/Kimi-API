# UIKit | UIAnimator

You use UIAnimator create animation to UIView components. 

```typescript

/**
 * Create curve animation.
 */
static curve(duration: number, animations: () => void, completion?: (finished: boolean) => void): void

/**
 * Create linear animation.
 */
static linear(duration: number, animations: () => void, completion?: (finished: boolean) => void): void

/**
 * Create spring animation.
 */
static spring(tension: number, friction: number, animations: () => void, completion?: () => void): void

/**
 * Create spring via bounciness and speed animation.
 */
static bouncy(bounciness: number, speed: number, animations: () => void, completion?: () => void): void
```
