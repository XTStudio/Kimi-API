# UIKit | UIDevice

An object that defines the properties associated with a hardware-based display.

```typescript
/**
 * Returns an object representing the current device.
 */
static readonly currentDevice: UIDevice

/**
 * The name identifying the device.
 */
readonly name: string

/**
 * The model of the device.
 */
readonly model: string

/**
 * The name of the operating system running on the device represented by the receiver.
 */
readonly systemName: string

/**
 * The current version of the operating system.
 */
readonly systemVersion: string

/**
 * An alphanumeric string that uniquely identifies a device to the app’s vendor.
 */
readonly identifierForVendor: UUID

```

## Relate

* [UUID](../Foundation/UUID.md)