# Q4 Explanation

1. `echo "sample log line" > app.log` created a sample application log. This gave the investigation a concrete file to monitor with file-descriptor tools.

2. `lsof` displayed open files across the system, while `lsof -p $$` narrowed the view to the current shell process. These commands show how Linux keeps track of files opened by each process.

3. `exec 3<app.log` opened the log as an extra file descriptor. The `/proc/$$/fd` listing then showed descriptor 3 pointing to `app.log`, which is a direct kernel-level view of file access.

4. The redirection commands demonstrated output control. `stdout.txt` captured normal output, `stderr.txt` captured the error stream, and `combined.txt` captured both by merging stderr into stdout.

5. `ulimit -a` displayed resource limits for the shell. The most relevant values here were the open-file limit and stack size, which affect how many files and processes a shell session can manage.
