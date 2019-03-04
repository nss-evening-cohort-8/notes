# I'de rather be using an IDE

## [Take a brief tutorial of Visual Studio 2017](https://tutorials.visualstudio.com/vs-get-started/intro)
It can feel [really cramped](https://twitter.com/dylanbeattie/status/832326857798348800) to code in Visual Studio if you don't know how to use it. Make sure that you "un-pin" any additional windows in Visual Studio that you find you're not using.

// TODO Explain docking windows because a student will inevitably accidentally undock a window and not know what to do with it.

### Some important windows that you will find in Visual Studio
* **_Solution Explorer_** allows you to browse the components of your application. Just like the file explorer in Visual Studio Code, this includes the files and folders that make up your application, but the Solution Explorer also includes your NuGet and npm dependencies, gives you access to graphical tools for editing your project files, and gives you the ability to drill into `*.cs` files, revealing the classes, methods and properties contained within them.
	* [The relationship between Projects & Solutions](https://docs.microsoft.com/en-us/visualstudio/ide/creating-solutions-and-projects)
* The **_Output Window_** displays a text log of every action that Visual Studio takes on your code. You can think about this window as displaying similar information as the `dotnet` command will print to the terminal. You'll find the success or errors of builds, package installations, debugging information, test results, and many other operations.
* The **_Code Editor_** is... where you edit the code.
	* [Learn a few of the Code Editor features](https://docs.microsoft.com/en-us/visualstudio/ide/writing-code-in-the-code-and-text-editor?view=vs-2017)  
	* [Learn the quickest ways to navigate through your code](https://docs.microsoft.com/en-us/visualstudio/ide/navigating-code)
	* Comment highlighted code <kbd>Ctrl</kbd>+<kbd>K,C</kbd>
	* Uncomment highlighted code <kbd>Ctrl</kbd>+<kbd>K,U</kbd>

### IntelliSense :bulb:
* To summon [IntelliSense](https://docs.microsoft.com/en-us/visualstudio/ide/using-intellisense?view=vs-2017), place your cursor where you want to activate it and press <kbd>Ctrl</kbd>+<kbd>.</kbd>
* Code completion
* Hover text/tooltips as documentation
* Red/Green squiggly underline is referring to the Error List.

### Refactor Rename <kbd>Ctrl</kbd>+<kbd>R,R</kbd>
* Preview Changes :point_up: , <kbd>Alt</kbd>+<kbd>P</kbd>

### Edit Mode vs Preview Mode
When you single-click on a file in the Solution Explorer, the file is open in _preview mode_. Only one file may be open at a time in preview mode. The currently open filename will be displayed in a tab on the far right side of the tab bar. Preview mode is handy for reading through several code files that you do not wish to edit.

As soon as you attempt to edit a file that's open it preview mode, it will move the file into edit mode.

This window normally appears at the bottom of Visual Studio. If you do not see it, You can open it by selecting the `Output` item in the `View` menu.

## [Debugger](https://docs.microsoft.com/en-us/visualstudio/debugger/debugger-feature-tour)
![debugger gif](https://docs.microsoft.com/en-us/visualstudio/debugger/media/dbg-tour-set-a-breakpoint.gif?view=vs-2017)
If you're not using the debugger already then [**_START NOW_**](https://docs.microsoft.com/en-us/visualstudio/debugger/index?view=vs-2019s). It is the single greatest tool a programmer can use. When you want to `console.log(something)`, now you will use a debugger instead.  
Even [in JavaScript](https://stackoverflow.com/a/66431).  
**Seriously, I never want to see another `console.log()` again.**
* Yellow arrow is the point of execution.  
The highlighted line has not been executed yet.
* Step Over <kbd>F10</kbd> (step to the next line)  
Step Into <kbd>F11</kbd> (step into this method)  
Step Out <kbd>Shift</kbd>+<kbd>F11</kbd> (step out of this method)
* Run to click
* Run to cursor <kbd>Ctrl</kbd>+<kbd>F10</kbd>

### Starting in Debug Mode

By default when you run your application in Visual Studio, it will run in Debug Mode. 

You can tell your application is running in debug mode, because the status bar at the bottom of the Visual Studio window will turn from blue to orange.


### Breakpoints

A breakpoint is a location in your code where you want to pause execution so you can examine the state of your application.

To set a breakpoint click on the vertical margin to the left of the Code Editor window. This clickable area is commonly called "the gutter." A red dot will appear in the margin and the code at that line will be highlighted in red.

To remove a breakpoint, click the red dot in the margin.

![Breakpoints](https://docs.microsoft.com/en-us/visualstudio/debugger/media/basicbreakpoint.png?view=vs-2017)

**Further reading**  
[Use Breakpoints in the Visual Studio Debugger](https://docs.microsoft.com/en-us/visualstudio/debugger/using-breakpoints?view=vs-2017)

### Autos and Locals Window

While you are stopped on a breakpoint, you can view the values of your variables with the **_Autos_** and **_Locals_** windows.  
You can also hover over variables with your mouse to peek at their current value.

![Autos and Locals](https://docs.microsoft.com/en-us/visualstudio/debugger/media/locals-filestream.png?view=vs-2017)

**Further reading**  
[Autos and Locals Windows](https://docs.microsoft.com/en-us/visualstudio/debugger/autos-and-locals-windows?view=vs-2017).

### Immediate Window

The **_Immediate Window_** is used to debug and evaluate expressions, execute statements, print variable values, and so forth. It allows you to enter expressions to be evaluated or executed during debugging.

![Immediate Window](./images/immediate.gif)

**Further reading**  
[Immediate Window](https://docs.microsoft.com/en-us/visualstudio/ide/reference/immediate-window?view=vs-2017)

## Call Stack

Use the **_Call Stack_** to view the entire execution "path" of the code up to the breakpoint.

![Callstack](https://docs.microsoft.com/en-us/visualstudio/debugger/media/dbg_basics_callstack_window.png?view=vs-2017)

**Further reading**  
[Call Stack Window](https://docs.microsoft.com/en-us/visualstudio/debugger/how-to-use-the-call-stack-window?view=vs-2017).

## More Debugging Windows

There are more windows that you can use while debugging your application. To see the entire list, and read more about each one, read the [Learn about Debugger Windows in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/debugger/debugger-windows?view=vs-2017) article.


## Further Reading
* https://tutorials.visualstudio.com/vs-get-started/debugging
* https://docs.microsoft.com/en-us/visualstudio/debugger/navigating-through-code-with-the-debugger?view=vs-2017 
* [Getting Started with the Debugger](https://msdn.microsoft.com/en-us/library/k0k771bt.aspx)
* [Visual Studio Keyboard Shortcuts](http://visualstudioshortcuts.com/2017/)
