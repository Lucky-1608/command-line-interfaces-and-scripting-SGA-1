# Q3 Explanation

1. `echo "Linux link test file" > original.txt` created the base file for the experiment. This file provided the contents that both link types would reference.

2. `ln original.txt hardlink.txt` created a hard link to the same inode. The important observation is that both names behave like equal references to the same file data.

3. `ln -s original.txt symlink.txt` created a symbolic link. Unlike a hard link, the symlink stores the path to the target rather than sharing the file’s inode.

4. `ls -li` and `stat` showed that `original.txt` and `hardlink.txt` shared inode 1310805, while `symlink.txt` had a different inode. This is the clearest way to distinguish hard links from symbolic links.

5. After `rm original.txt`, the hard link still opened the file contents because the inode still had one remaining reference. The symbolic link broke because it depended on the original file path.
