# Assets

This folder contains local asset folders which are mapped 
into running containers for cases where you want to store
the assets on the host.

The only important example is the Backups folders, the
others should not really be used.

## Backup

This folder is used to hold any backups that may be created
in local operation. It is mapped into the project at path
/app/backup, in all containers.

## Drupal assets

Both public and private Drupal files can be mapped to 
folders in assets, if you want to keep those things on
the host.

This is not necessary, and is more of an example.  These
asset folders should really be kept as unbound Docker 
volumes.
