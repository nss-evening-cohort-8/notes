# I'de rather be using an IDE
### Code Navigation
- [Code Navigation Tools](https://docs.microsoft.com/en-us/visualstudio/ide/navigating-code)

### [Take a brief tutorial of Visual Studio 2017](https://tutorials.visualstudio.com/vs-get-started/intro)  
It can feel [really cramped](https://twitter.com/dylanbeattie/status/832326857798348800) to code in Visual Studio if you don't know how to use it. Make sure that you "un-pin" any additional windows in Visual Studio that you find you're not using.

Explain docking windows.

### Some important windows that you will find in Visual Studio
- **_Solution Explorer_** allows you to browse the components of your application. Just like the file explorer in Visual Studio Code, this includes the files and folders that make up your application, but the Solution Explorer also includes your NuGet and npm dependencies, gives you access to graphical tools for editing your project files, and gives you the ability to drill into `*.cs` files, revealing the classes, methods and properties contained within them.
	- [The relationship between Projects & Solutions](https://docs.microsoft.com/en-us/visualstudio/ide/creating-solutions-and-projects)
- **_Output Window_** displays the results of various operations performed by Visual Studio. You can think about this window as displaying similar information as the `dotnet` command will print to the terminal. You'll find the results of builds, package installations, debugging information, test results, and many other operations.

[Learn a few of the Code Editor features](https://docs.microsoft.com/en-us/visualstudio/ide/writing-code-in-the-code-and-text-editor?view=vs-2017)

#### Edit Mode vs Preview Mode

When you single-click on a file in the Solution Explorer, the file is open in _preview mode_. Only one file may be open at a time in preview mode. The currently open filename will be displayed in a tab on the far right side of the tab bar. Preview mode is handy for reading through several code files that you do not wish to edit.

As soon as you attempt to edit a file that's open it preview mode, it will move the file into edit mode.

This window normally appears at the bottom of Visual Studio. If you do not see it, You can open it by selecting the `Output` item in the `View` menu.


# Debugging in Visual Studio

## Starting in Debug Mode

By default when you run your application in Visual Studio, it will run in Debug Mode. 

You can tell your application is running in debug mode, because the status bar at the bottom of the Visual Studio window will turn from blue to orange.


## Breakpoints

A breakpoint is a location in your code where you want to pause execution so you can examine the state of your application.

To set a breakpoint click on the vertical margin to the left of the Code Editor window. A red dot will appear in the margin and the code at that line will be highlighted in red.

To remove a breakpoint, click the red dot in the margin.

![Breakpoints](./images/breakpoint.gif)

**Further reading**
[Use Breakpoints in the Visual Studio Debugger](https://docs.microsoft.com/en-us/visualstudio/debugger/using-breakpoints?view=vs-2017)

## Autos and Locals Window

When you are stopped on a breakpoint Studio, you can view the values of your variables with the Autos and Locals windows.

![Autos and Locals](./images/autos_locals.gif)

**Further reading**
[Autos and Locals Windows](https://docs.microsoft.com/en-us/visualstudio/debugger/autos-and-locals-windows?view=vs-2017).

## Immediate Window

The Immediate window is used to debug and evaluate expressions, execute statements, print variable values, and so forth. It allows you to enter expressions to be evaluated or executed during debugging.

![Immediate Window](./images/immediate.gif)

**Further reading**
[Immediate Window](https://docs.microsoft.com/en-us/visualstudio/ide/reference/immediate-window?view=vs-2017)

## Call Stack

Use the callstack to view the entire execution "path" to the code up to the breakpoint.

![Callstack](./images/callstack.gif)

**Further reading**
[Call Stack Window](https://docs.microsoft.com/en-us/visualstudio/debugger/how-to-use-the-call-stack-window?view=vs-2017).

## More Debugging Windows

There are more windows that you can use while debugging your application. To see the entire list, and read more about each one, read the [Learn about Debugger Windows in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/debugger/debugger-windows?view=vs-2017) article.


## Further Reading
* https://tutorials.visualstudio.com/vs-get-started/debugging
* https://docs.microsoft.com/en-us/visualstudio/debugger/navigating-through-code-with-the-debugger?view=vs-2017 
* [Getting Started with the Debugger](https://msdn.microsoft.com/en-us/library/k0k771bt.aspx).



### [Debugger](https://docs.microsoft.com/en-us/visualstudio/debugger/debugger-feature-tour)  
https://docs.microsoft.com/en-us/visualstudio/get-started/csharp/tutorial-debugger?view=vs-2017  
If you're not using the debugger already then [**_START NOW_**](https://docs.microsoft.com/en-us/visualstudio/debugger/index?view=vs-2019s). It is the single greatest tool a programmer can use. When you want to `console.log(something)`, now you will use a debugger instead. Even [in JavaScript](https://stackoverflow.com/a/66431). **Seriously, I never want to see another `console.log()` again.**
- Yellow arrow is the point of execution. The highlighted line has not been executed yet.
- Call Stack shows current code path at point of execution.
- Locals, Immediate Window, & Watch.
	> Also, hovering over variables and using the mouse, but why do that when you have [hotkeys](http://visualstudioshortcuts.com/2017/) and search (<kbd>Ctrl</kbd>+<kbd>Q</kbd>)?
- Step Over <kbd>F10</kbd>, Step Into <kbd>F11</kbd>, and Step Out <kbd>Shift</kbd>+<kbd>F11</kbd>
- Run to click
- Run to cursor (<kbd>Ctrl</kbd>+<kbd>F10</kbd>)

### Intellisense
- Code completion
- Hover text/tooltips as documentation
- Red/Green squiggly underline is referring to the Error List.
- :bulb: - (<kbd>Ctrl</kbd>+<kbd>.</kbd>)

### Refactor Rename (<kbd>Ctrl</kbd>+<kbd>R,R</kbd>)
- Preview Changes :point_up: , (<kbd>Alt</kbd>+<kbd>P</kbd>)
