# UIKIt | UIAnimator

You use UIAnimator create animation to UIView components. 

```typescript
/**
 * Always use shared instance.
 */
static shared: UIAnimator

/**
 * Create linear animation.
 */
linear(duration: number, animations: () => void, completion?: (finished: boolean) => void): void

/**
 * Create spring animation.
 */
spring(tension: number, friction: number, animations: () => void, completion?: () => void): void
```