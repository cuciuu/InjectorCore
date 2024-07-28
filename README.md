# InjectorCore

InjectorCore is a .NET library designed to facilitate (ANY DLL) injection into running processes.

## Features

- Easy DLL injection
- Detailed logging for debugging
- Supports a variety of Win32 API functions

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/cuciuu/InjectorCore.git
    ```
2. Open the project in Visual Studio.
3. Build the project to generate the library.

## Usage

### Basic Usage

```csharp
using System;
using InjectorCore;

class Program
{
    static void Main()
    {
        try
        {
            bool result = Injection.Run("targetProcessName", "path_to_your_dll.dll");
            if (result)
            {
                Console.WriteLine("DLL injection successful!");
            }
        }
        catch (Exception ex)
        {
            Console.WriteLine($"Error: {ex.Message}");
        }
    }
}
```
Replace "targetProcessName" with the name of the process you want to inject the DLL into and "path_to_your_dll.dll" with the path to your DLL file.

## Contributing

Contributions are welcome! Please read the contributing guidelines first.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

If you have any questions or feedback, please open an issue or contact us at [your email].

#### API.md
```markdown
# InjectorCore API Documentation

## Injection Class

### Methods

#### Run(string processName, string pathToDLL)
- **Description**: Injects a DLL into the specified process.
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
```
