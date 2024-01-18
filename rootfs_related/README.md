References for creating rootfs

https://github.com/firecracker-microvm/firecracker/blob/main/docs/rootfs-and-kernel-setup.md
https://github.com/carlosedp/riscv-bringup/blob/master/Ubuntu-Rootfs-Guide.md

Create empty rootfs and then copy files:

$ dd if=/dev/zero of=rootfs.ext4 bs=1M count=50
$ mkfs.ext4 rootfs.ext4
$ mkdir /tmp/my-rootfs
$ sudo mount rootfs.ext4 /tmp/my-rootfs

now copy files and unmount.
