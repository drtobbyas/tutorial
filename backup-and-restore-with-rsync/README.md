# Backup And Restore using Rsync

## To Backup

## Install Rsync
```bash
sudo apt install rsync

```

### Create Backup Directory

```bash

mkdir -p /backup

```

### Create Rsync Backup

```bash
rsync -aAXv --exclude={"/backup","/dev","/proc","/sys","/tmp","/run","/mnt","/media","/lost+found"} / /backup/

```

### Create Archive of Backup

```bash

tar -czvf backup.tar.gz -C /backup .

```

## To Restore

### Create Restore Directory

```bash

sudo mkdir -p /restore

```

### Move backup archive to restore directory

```bash

sudo mv /path/to/backup.tar.gz /restore

```

### Unzip the backup file

```bash

sudo tar -xzvf /restore/backup.tar.gz -C /


```

### Reboot System

```bash

sudo reboot

```