Despite the fact that C++ is now supported for kernel development inWindows, there is still no basic c++ runtime for the kernel. And of course the endless debate about the merits of C++ continues on the ntdev site.
  
I'll let you know right now that I am on the side of truth, liberty, mom, apple-pie, the american way, and C++ in the kernel. I figure one way to end the debate is to make the use of C++ pervasive. As a step in that direction, here is at least part of the missing runtime infrastructure that is required for full C++ support, a C++ kernel runtime library.

What's missing in the kernel is support for global new and delete, initialization of global class objects, and C++ exception handling. (There is probably a lot of other stuff missing as well, but this is the basic list.) So a while back I concocted a simple C++ kernel runtime library. I

The package is open source, freely redistributable (under the MIT license), and available here for downloading.  Comments, contributions, money, always gladly accepted. 

What's new?
•The license has changed from the awful lgpl to what I originally intended, an actual open source license (MIT license.)
•no more MSI, just a zip file.

 

Instructions.

Step 1.

Download the latest version here, this link is to a zip file for the source code distribution.

Step 2.

Install the sources as appropriate for yourt project needs. Modify the SOURCES file for the library as appropriate.

Step 3.

Modify your Sources files to link with the library.

Step 4.

Include the kernel c++ header file htscpp.h in your source files and modify your DriverEntry routine, renaming your DriverEntry routine from DriverEntry to CPP_DRIVER_ENTRY.  

Step 5.

Build your driver.

Windows Kernel C++ Runtime
