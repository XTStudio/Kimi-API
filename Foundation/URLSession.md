# Foundation | URLSession

## URLSession

An object that coordinates a group of related network data transfer tasks.

```typescript

/**
 * The shared singleton session object.
 */
static readonly shared: URLSession

/**
 * Creates a task that retrieves the contents of the specified URLString or URL or URLRequest, then calls a handler upon completion.
 */
dataTask(req: string | URL | URLRequest, complete: (data?: Data, response?: URLResponse, error?: Error) => void): URLSessionTask

```

## URLSessionTask

A task, like downloading a specific resource, performed in a URL session.

```typescript
/**
 * The current state of the task—active, in the process of being canceled, or completed.
 */
readonly state: URLSessionTaskState

/**
 * The number of bytes that the task expects to receive in the response body.
 */
readonly countOfBytesExpectedToReceive: number

/**
 * The number of bytes that the task has received from the server in the response body.
 */
readonly countOfBytesReceived: number

/**
 * The number of bytes that the task expects to send in the request body.
 */
readonly countOfBytesExpectedToSend: number

/**
 * The number of bytes that the task has sent to the server in the request body.
 */
readonly countOfBytesSent: number

/**
 * Cancels the task.
 */
cancel(): void

/**
 * Resumes the task, if it is suspended.
 */
resume(): void
```

## URLSessionTaskState

```typescript
enum URLSessionTaskState {
    /**
     * The task is currently being serviced by the session.
     */
    running,
    /**
     * The task is currently paused.
     */
    suspended,
    /**
     * The task has received a cancel message.
     */
    cancelling,
    /**
     * The task has completed (without being canceled), and the task's delegate receives no further callbacks.
     */
    completed,
}
```
