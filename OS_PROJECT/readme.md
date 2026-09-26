1. Problem Statement:-
Traditional file distribution systems may face performance problems when many clients request files at the same time. If requests are handled one after another, clients have to wait, which increases response time. The project addresses this problem by creating a separate child process for each file request. The server supports both reading existing files and writing data to files, while using pipes for communication between the parent and child processes. Proper file descriptor and process management is used to maintain reliable file operations.

2. Objectives:-

1. To design and implement a Linux-based high-concurrency file server.

2. To handle multiple read and write requests using separate child processes.

3. To use fork() and anonymous pipes for process creation and inter-process communication.

4. To understand and demonstrate Linux file descriptors and file I/O using open(), read(), write() and close().

5. To demonstrate proper child-process management using waitpid() and wait().

3. Overall flow: Request received → pipe created → child process created using fork() → parent sends request through pipe → child reads request → file opened → read/write operation performed → file and pipe descriptors closed → child terminates → next request handled.

