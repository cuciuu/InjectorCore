
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

If you have any questions or feedback, please open an issue or contact us at [cuciuloll@gmail.com]