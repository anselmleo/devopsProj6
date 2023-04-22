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

<img width="495" alt="Screen Shot 2023-04-21 at 5 51 44 PM" src="https://user-images.githubusercontent.com/30025376/233806835-9513fe34-5156-4d69-b9da-686f82505321.png">

- Step 10: Backup logs and mount to logs lv
- Step 11: mount db lv to /var/www/db

<img width="731" alt="Screen Shot 2023-04-21 at 9 36 18 PM" src="https://user-images.githubusercontent.com/30025376/233806947-d953b604-828a-4965-bb60-3a15f2acd4b1.png">

- Step 12: Update the /etc/fstab file to make mount permanent
- Step 13: Test mount
- Step 14: Back on the webserver, install apache and it's dependencies
- Step 15: Start and enable Apache webserver
- Step 16: Install php and it's dependencies
- Step 17: Make wordpress directory, download wordpress via curl
- Step 18: Uncompress wordpress and delete compression file
- Step 19: Rename wordpress config file

<img width="629" alt="Screen Shot 2023-04-22 at 8 47 02 PM" src="https://user-images.githubusercontent.com/30025376/233807018-57210849-db75-4d87-a4f4-f14877c6fa94.png">

- Step 20: Copy recursively to /var/www/html directory
- Step 20.5 Update wp-config file with correct username, password and host
- Step 21: Back on DB server, install mysql server
- Step 22: Start and enable mysql server

<img width="486" alt="Screen Shot 2023-04-22 at 9 41 50 PM" src="https://user-images.githubusercontent.com/30025376/233807076-2bf5221e-63fc-47a9-934b-4cc4466dfbfe.png">

- Step 23: Create a wordpress db (To enable wordpress application connection)
- Step 24: Create a remote mysql user and assign privileges to the wordpress databases
- Step 25: Test remote connection works

<img width="486" alt="Screen Shot 2023-04-22 at 9 41 50 PM" src="https://user-images.githubusercontent.com/30025376/233807076-2bf5221e-63fc-47a9-934b-4cc4466dfbfe.png">

- Step 26: Launch app by pasting public ip address of webserver on browser and /wordpress e.g: <public-ip-webserver>/wordpress

<img width="1440" alt="Screen Shot 2023-04-22 at 9 52 38 PM" src="https://user-images.githubusercontent.com/30025376/233807134-96eaa111-3af0-4ac5-87b4-a55678707d09.png">

- Step 27: If error connecting to database? Check wp-config.php file and confirm your database credentials match the actual remote db credentials

<img width="1153" alt="Screen Shot 2023-04-22 at 10 01 27 PM" src="https://user-images.githubusercontent.com/30025376/233807314-156f7804-4a25-4a5d-86f0-315f2a767e7f.png">

