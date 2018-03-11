This script is intended as a automated backuptool used with cron and depends on [own-snapshot](https://github.com/m-k-r/own-snapshot).  
It uses elements and jobs to define mode, names, timestamp format, source and target. Both Source and Target can be offside.  
Snapshots are supported for zfs, kvm (qm), files, directories, mysql and postgresql. The snapshots can be zfs, btrfs or file-based.  
zfs, btrfs and qm use their own tools, directories and files use rsync to copy and files, mysql and pgsql can be encrypted.  
They are encrypted on the source server before they are copied to the targetserver and disk.

### usage

**own-backup -e** $ELEMENT

**additional:**  
-c : **initial** config, **upgrade** elements  
-d : **check**, or show **export** and **import** variables of a dump, or **create** a dump  
-f : overrides the frequency  
-g : overrides the target  
-j : job. atm a predefined list of arguments. later a list of multiple elements with predefined arguments  
-m : copies multiple (or all) newer snapshots instead of the last  
-n : overrides limit for snapshots  
-o : output: commands, datasets, snapshots, snapvars, full  
-r : rollback  
-s : overrides snapshotname  
-t : overrides the date  


Example configs can be found in the template directory.
