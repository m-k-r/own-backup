This script is intended as a automated backuptool used with cron and depends on [own-snapshot](https://github.com/m-k-r/own-snapshot).

It uses config files to define mode, names, timestamp format, source and target. Both Source and Target can be offside.

It has a build in snapshot management and can be used with btrfs, zfs, kvm (qm), files, directories, mysql and postgresql.

zfs, btrfs and qm use their own tools, directories and files use rsync to copy and files, mysql and pgsql can be encrypted. They are encrypted on the source server before they are copied to the targetserver and disk.

### usage

**own-backup -c** $CONFIG **-d** $DEBBUG

**additional:**  
-m : copies multiple snapshots instead of the last.  
-r : rollback. Source and target are swapped. No new snapshots are created  
-e : overrides the target.  
-f : overrides the frequency.  
-n : overrides the number for snapshots.  
-s : overrides the snapshotname  
-t : overrides the date

Example configs can be found in the template directory.
