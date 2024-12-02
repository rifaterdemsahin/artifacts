# Creating Dynamic Link Libraries in CodeSpaces

This guide will help you create a Dynamic Link Library (DLL) using the `hello.cs` file in GitHub Codespaces.

## Steps

1. **Open Codespaces**: Start your Codespaces environment.

2. **Create the `hello.cs` File**:
    ```csharp
    using System;

    class Program
    {
        static void Main()
        {
            Console.WriteLine("Hello, World! New Comers");
        }
    }
    ```

3. **Create a New Project**:
    Open the terminal in Codespaces and run the following command to create a new class library project:
    ```sh
    dotnet new classlib -n HelloWorldLibrary
    ```

4. **Move `hello.cs` to the Project Folder**:
    Move your `hello.cs` file into the `HelloWorldLibrary` folder:
    ```sh
    mv hello.cs HelloWorldLibrary/
    ```

5. **Modify `hello.cs`**:
    Update `hello.cs` to be a class library:
    ```csharp
    using System;

    public class HelloWorld
    {
        public static void Greet()
        {
            Console.WriteLine("Hello, World! New Comers");
        }
    }
    ```

6. **Build the DLL**:
    Navigate to the `HelloWorldLibrary` folder and build the project:
    ```sh
    cd HelloWorldLibrary
    dotnet build
    ```

7. **Output**:
    The DLL will be created in the `bin/Debug/netstandard2.0` directory.

You have successfully created a Dynamic Link Library using `hello.cs` in GitHub Codespaces.