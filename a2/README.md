## Backup shell command ##

backup.sh <specified_directory> <target_directory>

specified = directory to be compressed and saved
target = target location where compressed directory is saved


## PURPOSE OF THE COMMAND ##

This command automates the process of backing up a directory. 
It compresses a specified directory and then saves it to a target directory.


## WHY IS THIS COMMAND USEFUL? ##

* Easily and quickly make backup of directories
* Directories are stored in compressed format, saving on storage space and allowing easy restoration
* Can be used periodically to make many date-stamped versions of directory (if earlier version is needed)

## HOW TO USE THIS COMMAND ##

This command takes in the specified directory that will be saved in a target directory. The command must be used from the parent directory of the specified directory.

Example: backup.sh data_folder backup_folder

This saves a copy of data_folder to backup_folder. If you cd into backup_folder, then you will see a compressed and date-stamped copy of data_folder. 

To extract the files/directories located in data_folder, you can use: 
tar -xzf ~/backup_folder/data_folder-2024-07-03.tar.gz -C ~/backup_folder.


##Terminal Example##

cd

ls

bin  cs131  cs131_backup  index.html  taxiData

backup.sh taxiData cs131_backup

Backup of taxiData completed at cs131_backup/taxiData_2024-07-03.tar.gz

cd cs131_backup

ls

taxiData_2024-07-03.tar.gz

tar -xzf ~/cs131_backup/taxiData_2024-07-03.tar.gz -C ~/cs131_backup

ls

dataset  taxiData_2024-07-03.tar.gz

more dataset

TAXI DATA GOES HERE
