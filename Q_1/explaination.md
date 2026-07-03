# Q1 Explanation

1. `whoami` confirmed the current login user. It showed that the active account is `codespace`.

2. `id` displayed the user ID, group ID, and supplemental groups. This confirmed the account has access to several development-related groups in the container.

3. `echo "$SHELL"` printed the shell in use. The result `/bin/bash` shows Bash is the active shell.

4. `pwd` showed the current working directory. The output `/` means the session was at the filesystem root when the verification was run.

5. `ls -ls` listed the contents of the root directory with permissions and sizes. This gave a quick view of the Linux filesystem layout and mounted locations.

6. `curl -s --max-time 10 https://youtube.com > /dev/null && echo "Network: youtube.com reachable"` tested external connectivity. The success message confirmed that outbound network access is available.
