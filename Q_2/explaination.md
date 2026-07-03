# Q2 Explanation

1. `mkdir -p secure_workspace/{docs,src,logs}` created the required project structure. The `-p` option ensured the directory tree was built in one step without errors if any parent already existed.

2. `touch` created the empty project files used for documentation, application code, and logging. These files gave the workspace the expected starting layout for the assignment.

3. `ls -ld secure_workspace secure_workspace/*` showed the initial permissions and ownership. The directories began with open default permissions, which is why they needed to be restricted.

4. `chmod 750 secure_workspace` and `chmod 750 secure_workspace/docs secure_workspace/src secure_workspace/logs` limited directory access. This protects project data by allowing the owner full control while preventing unauthorized write access.

5. `chmod 640 secure_workspace/docs/plan.txt secure_workspace/src/app.txt secure_workspace/logs/activity.log` was intended to secure the files. In the captured output, `activity.log` stayed world-readable/writable because the command was truncated in the screenshot, so the report records that mismatch explicitly.

6. `umask` returned `0022`. That default mask explains why newly created files start with standard permissions that still require hardening for a secure workspace.
