# Get-sysdiagnose-log
This small shell script file under macOS. 
When you file a radar for a bug on one of Apple’s platforms, you should (usually) always attach a sysdiagnose. 

A sysdiagnose provides a lot of helpful information for the person who is trying to understand how the bug happened. 

Amongst other things, it contains logs from various parts of the OS, and all recent crash logs.  

Without it, the person on the other end of your report inside Apple may not be of much help.

On macOS, sysdiagnose is fairly well-documented. 
You can run it from the command line via sudo sysdiagnose, which will place the resulting .tar.gz file in /var/tmp/.

It can take up to 10 minutes to complete and there are no visual indicators that anything is happening. 

Be patient and continue with whatever work you were doing. The report will contain tons of logs, system statistics, and other diagnostic information. 

Note: On all systems, the device will become unresponsive during parts of generating the sysdiagnose and the generated .tar.gz will usually be around 200-300 MB.

What sysdiagnose collects: 

1.A spindump of the system. 

2.Several seconds of fs_usage ouput. 

3.Several seconds of top output. 

4.Data about kernel zones. 

5.Status of loaded kernel extensions. 

6.Resident memory usage of user processes. 

7.Recent system logs. 

8.A System Profiler report. 

9.Recent crash reports. 

10.Disk usage information. 

11.I/O Kit registry information. 

12.Network status. 

13.If a specific process is supplied as an argument: list of mal-loc-allocated buffers in the process's heap is collected.

14.If a specific process is supplied as an argument: data about unreferenced malloc buffers in the process's memory is col- lected. 

15.If a specific process is supplied as an argument: data about the virtual memory regions allocated in the process. 
