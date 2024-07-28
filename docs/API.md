# InjectorCore API Documentation

## Injection Class

### Methods

#### Run(string processName, string pathToDLL)
- **Description**: Injects a DLL into the specified process. Supports both 64-bit and 32-bit processes.
- **Parameters**:
  - `processName` (string): The name of the process to inject the DLL into.
  - `pathToDLL` (string): The path to the DLL file to be injected.
- **Returns**: (bool) `true` if the injection is successful.
- **Exceptions**: Throws `ApplicationException` if the process is not found, if the process cannot be opened, or if there are issues during the injection process.

#### Init()
- **Description**: Initializes the internal state for the injection process.

#### InjectDLL(string path)
- **Description**: Injects the DLL into the target process.
- **Parameters**:
  - `path` (string): The path to the DLL file to be injected.

#### GetProcessPID(string processName)
- **Description**: Retrieves the PID of the specified process.
- **Returns**: (UInt32) The PID of the process, or `UInt32.MinValue` if not found.

## Enums

### ProcessAccessFlags
- **Description**: Flags for process access levels.

### AllocationType
- **Description**: Flags for memory allocation types.

### MemoryProtection
- **Description**: Flags for memory protection types.
