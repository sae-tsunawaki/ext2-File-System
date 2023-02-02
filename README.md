# Hey! I'm Filing Here

 Implementation of a 1 MiB ext2 file system with 2 directories, 1 regular file, and 1 symbolic link.

## Building

To build, simply run:
make

## Running

To compile: 
./ext2-create 

To mount: 
mkdir mnt 
sudo mount -o loop cs111-base.img mnt

Example output of 'ls -ain' of my mounted filesystem: 
total 7
      2 drwxr-xr-x 3    0    0 1024 Jun  4 17:54 .
1097792 drwxr-xr-x 3 1000 1000 4096 Jun  4 17:55 ..
     13 lrw-r--r-- 1 1000 1000   11 Jun  4 17:54 hello -> hello-world
     12 -rw-r--r-- 1 1000 1000   12 Jun  4 17:54 hello-world
     11 drwxr-xr-x 2    0    0 1024 Jun  4 17:54 lost+found

## Cleaning up

To unmount the filesystem:
sudo umount mnt

To remove the mount directory:
rmdir mnt 

To clean up all binary files:
make clean 
