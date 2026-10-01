1. Problem Statement:-
Without a proper file server, managing and accessing files for multiple clients can be difficult and time-consuming. Clients may have to wait for files to be accessed or updated, especially when many clients need files at the same time. A file server makes file handling easier by providing a central place to store files and allowing multiple clients to access or update the required files more efficiently.

2. Objectives:-

1. To design and implement a Linux-based high-concurrency file server.

2. To handle multiple read and write requests using separate child processes.

3. To use fork() and anonymous pipes for process creation and inter-process communication.

4. To understand and demonstrate Linux file descriptors and file I/O using open(), read(), write() and close().

5. To demonstrate proper child-process management using waitpid() and wait().

3. Overall flow: Request received → pipe created → child process created using fork() → parent sends request through pipe → child reads request → file opened → read/write operation performed → file and pipe descriptors closed → child terminates → next request handled.

