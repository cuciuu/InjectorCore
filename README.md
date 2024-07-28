# InjectorCore

<p align="center">
  <img src="https://github.com/user-attachments/assets/824f5406-05cd-4204-8eb0-9cf086cb965a" alt="logo" width="45" height="45" />
</p>

InjectorCore is a .NET library designed to facilitate DLL injection into running processes, supporting both 64-bit and 32-bit processes.

## Features

- 🛠️ **Easy DLL injection**
- 📋 **Detailed logging for debugging**
- ⚙️ **Supports a variety of Win32 API functions**
- 🖥️ **Compatible with both 64-bit and 32-bit processes**

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/cuciuu/InjectorCore.git
    ```
2. Open the project in Visual Studio 2017 or later.
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
If you have any questions or feedback, please open an issue or contact us at [cuciuloll@gmail.com].
