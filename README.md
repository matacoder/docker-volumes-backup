# Docker Volumes Backup to remote server
1. Set up envs: IP_HOST, IP_RECEIVER, SSH_KEY, TELEGRAM_TO, TELEGRAM_TOKEN
2. Make sure you have installed Docker via official guide and you have your volumes at `/var/lib/docker/volumes`
3. If you use ISPMANAGER 6 on RECEIVER side you are okay. Otherwise change path at line 28 of GitHub Actions
4. Well, I assume you have your ISPMANAGER 6 sites backed up via S3 or something

# Zipping backup
Just a memo: `tar czf volumes.tar.gz -C /var/lib/docker/volumes .`

# Unzipping backup
Run `tar -xf volumes.tar.gz -C /var/lib/docker/volumes .` to restore

# One last thing
You're awesome. You're thinking of backups. Kids will be proud.
Have a nice day.
