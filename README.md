# linux-lvm-project
# LVM Creation, Backup and Restore Project

## Steps Done:
1. Created Physical Volume (PV)
2. Added PV into Volume Group `vg1`
3. Created Logical Volume `lv1`
4. Formatted LV with ext4 filesystem
5. Mounted temporary and retrieved UUID
6. Configured persistent mount using `/etc/fstab`
7. Took LVM metadata backup using `vgcfgbackup`
8. Restored metadata using `vgcfgrestore`

## Useful Commands
pvcreate /dev/sdb
vgcreate vg1 /dev/sdb
lvcreate -L 5G -n lv1 vg1
mkfs.ext4 /dev/vg1/lv1
mount /dev/vg1/lv1 /mnt
blkid
vi /etc/fstab
vgcfgbackup
vgcfgrestore

## Skills Learned
✔ Storage allocation  
✔ LVM components (PV, VG, LV)  
✔ Persistent mount configuration  
✔ Backup & restore operations  
