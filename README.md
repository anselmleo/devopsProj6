# devopsProj6
setup logical volumes like a pro


### DEMO

- Step 1: Setup and Instatiate new RedHat instance
- Step 2: Allow ssh, https and http
- Step 3: Create three volumes

<img width="1376" alt="Screen Shot 2023-04-17 at 8 07 29 PM" src="https://user-images.githubusercontent.com/30025376/233720065-5faef551-3404-443a-987d-2b3bbae9c59b.png">

- Step 4: Attach volumes to webserver instance
- Step 5: Create a partition on each of them using gdisk
- Step 6: Install LVM2 and create physical volumes on each of the partitions
- Step 7: Create a volume group of the physical volumes
- Step 8: Make two logical volumes from the volume group => 1. /var/www/html and 2. /var/logs
- Step 9: Format new volumes with ext4 file system
- Step 10: Backup logs and mount to logs lv
- Step 11: mount db lv to /var/www/db
- Step 12: Update the /etc/fstab file to make mount permanent
- Step 13: Test mount
- Step 14: Back on the webserver, install apache and it's dependencies
- Step 15: Start and enable Apache webserver
- Step 16: Install php and it's dependencies
- Step 17: Make wordpress directory, download wordpress via curl
- Step 18: Uncompress wordpress and delete compression file
- Step 19: Rename wordpress config file
- Step 20: Copy recursively to /var/www/html directory
- Step 20.5 Update wp-config file with correct username, password and host
- Step 21: Back on DB server, install mysql server
- Step 22: Start and enable mysql server
- Step 23: Create a wordpress db (To enable wordpress application connection)
- Step 24: Create a remote mysql user and assign privileges to the wordpress databases
- Step 25: Test remote connection works

