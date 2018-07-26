# UIKIt | UIAnimator

You use UIAnimator create animation to UIView components. 

```typescript

/**
 * Create linear animation.
 */
static linear(duration: number, animations: () => void, completion?: (finished: boolean) => void): void

/**
 * Create spring animation.
 */
static spring(tension: number, friction: number, animations: () => void, completion?: () => void): void
```
