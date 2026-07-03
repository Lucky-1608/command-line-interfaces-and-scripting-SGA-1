# Q5 Explanation

1. `lsblk` listed the available block devices and partitions. This gave a quick overview of the storage layout available in the environment.

2. `mount | head -5` showed the active mount points and filesystem types. The output confirms that the workspace is running inside a container-style Linux environment with overlay and virtual filesystems.

3. `df -h` reported disk usage in human-readable form. This is the most useful command for spotting which mount points are close to full, and `/vscode` was the largest percentage in the captured output.

4. `df -i` checked inode utilization. The inode usage remained low, which means file-count exhaustion is not an immediate storage issue here.

5. The report file is meant to document the findings clearly for submission. If you open and edit it in vi, it satisfies the assignment’s documentation requirement while keeping the content aligned with the captured results.
