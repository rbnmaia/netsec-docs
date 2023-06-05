# Windows PE

### Windows Architecture

![](https://malwareunicorn.org/re101/img/a49e773f13968e92.png)

#### User-mode vs. Kernel Mode[ \[1\]](https://msdn.microsoft.com/en-us/windows/hardware/drivers/gettingstarted/user-mode-and-kernel-mode?f=255\&MSPPError=-2147217396)

* In user-mode, an application starts a user-mode process which comes with its own private virtual address space and handle table
* In kernel mode, applications share virtual address space.

This diagram shows the relationship of application components for user-mode and kernel-mode.

### PE Header

The PE header provides information to operating system on how to map the file into memory. The executable code has designated regions that require a different memory protection (RWX)

* Read
* Write
* Execute

![](https://malwareunicorn.org/re101/img/faff0917056c4dc6.png)

Here is a hexcode dump of a PE header we will be working with.

### Memory Layout

* **Stack** - region of memory is added or removed using "last-in-first-out" (LIFO) procedure[\[2\]](https://en.wikipedia.org/wiki/Stack\_\(abstract\_data\_type\))
* **Heap** - region for dynamic memory allocation[\[3\]](https://en.wikipedia.org/wiki/Heap\_\(data\_structure\))
* **Program Image** - The PE executable code placed into memory
* **DLLs** - Loaded DLL images that are referenced by the PE
* **TEB** - Thread Environment Block stores information about the current running thread(s)[\[4\]](https://en.wikipedia.org/wiki/Win32\_Thread\_Information\_Block)
* **PEB** - Process Environment Block stores information about loaded modules and processes.[\[5\]](https://en.wikipedia.org/wiki/Process\_Environment\_Block)

![](https://malwareunicorn.org/re101/img/dd272ca01a1a1780.png)

### The Stack

* Data is either pushed onto or popped off of the stack data structure
* **EBP** - Base Pointer is the register that used to store the references in the stack frame

![](https://malwareunicorn.org/re101/img/12ddbf0c041574ca.png)
