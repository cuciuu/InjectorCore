# InjectorCore

InjectorCore is a .NET library designed to facilitate DLL injection into running processes.

## Features

- Easy DLL injection
- Detailed logging for debugging
- Supports a variety of Win32 API functions

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/InjectorCore.git
    ```
2. Open the project in Visual Studio 2017.
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
