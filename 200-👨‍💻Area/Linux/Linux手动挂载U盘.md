先使用 more /proc/partitions 命令查看系统的硬盘和分区情况
再建立挂载点: sudo mkdir -p /mnt/udisk1/
再挂载U盘： sudo mount -t vfat /dev/sdb4 /mnt/udisk1/

解除挂载：sudo umount /mnt/udisk1/