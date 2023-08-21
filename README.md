# BadFilter

## Just a test Windows minifilter driver

Introduces latency in FileIO Create operations so that the results can be profiled with Windows Performance Toolkit and studied to learn more about troubleshooting minifilter performance issues on Windows.

## To install and use:

Compile project to .sys driver file, .cat files and .inf file.

Right-Click chadsbadfilter.inf file->Install

Open admin cmd.exe and **fltmc load chadsbadfilter** This will load the filter to all attached volumes. This will slow down the OS overall. You can test on 1 volumne i.e. D: drive using the following.

**fltmc detach chadsbadfilter C: "chadsbadfilter Instance"** This will remove the instance of the filter on the C: drive so that the OS is still fast but the D: drive is slow, so testing can be done.

To change the amount of performance impact change the clock resolution of Windows using tools that can accomplish this.
