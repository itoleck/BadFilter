# BadFilter

## Just a test Windows minifilter driver

Introduces latency in FileIO Create operations so that the results can be profiled with Windows Performance Toolkit and studied to learn more about troubleshooting minifilter performance issues on Windows.

## To install and use:

Compile project to .sys driver file, .cat files and .inf file.

Right-Click .inf file->Install

Open admin cmd.exe and **fltmc load chadsbadfilter**

To change the amount of performance impact change the clock resolution of Windows using tools that can accomplish this.
