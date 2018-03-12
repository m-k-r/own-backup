This script is intended as a automated backuptool used with cron and depends on [own-snapshot](https://github.com/m-k-r/own-snapshot).  
Elements and jobs (atm modifier, later multiple elements and modifier) are used to define mode, names, timestamp format, source and target. Both Source and Target can be offside.  
Snapshots are supported for zfs, kvm (qm), files, directories, mysql and postgresql and stored as zfs, btrfs or file.  
zfs, btrfs and qm use their own tools, directories and files are snapshotted via rsync. Additionally files, mysql and pgsql can be encrypted. The encryption takes place on the source server before copying to the target server or disk.

### usage

**own-backup -e** $ELEMENT (**-j** $JOB)

**additional:**  
-c : **initial** config, **upgrade** elements  
-d : **check**, or show **export** and **import** variables of a dump, or **create** a dump  
-f : overrides the frequency  
-g : overrides the target  
-m : copies multiple (or all) newer snapshots instead of the last  
-n : overrides limit for snapshots  
-o : output: commands, datasets, snapshots, snapvars, full  
-r : rollback  
-s : overrides snapshotname  
-t : overrides the date  

Example configs can be found in the template directory.
