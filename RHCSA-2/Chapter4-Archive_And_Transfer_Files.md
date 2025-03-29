## Archive and Transfer Files ##

* `rsync -a` (rchive mode) preserve most characteristic of a file but not hardlinks.
* `rsync -H` preserve hardlinks.
* `rsync -X ` preserve selinux context.