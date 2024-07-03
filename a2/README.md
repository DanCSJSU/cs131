## Backup shell command ##

backup.sh <specified_directory> <target_directory>

specified = directory to be compressed and saved
target = target location where compressed directory is saved


## PURPOSE OF THE COMMAND ##

This command automates the process of backing up a directory. 
It compresses a specified directory and then saves it to a target directory.


## WHY IS THIS COMMAND USEFUL? ##

This command is useful because it allows the user to quickly and easily create a backup of a directory. This ensures that an important directory is safely stored in a compressed format, saving on storage space and allowing easy restoration if necessary. The user can periodically use this command and may have many date-separated versions of a directory, in case an earlier version is needed.

## HOW TO USE THIS COMMAND ##

This command takes in the specified directory that will be saved in a target directory. The command must be used from the parent directory of the specified directory.

Example: backup.sh data_folder backup_folder

This saves a copy of data_folder to backup_folder. If you cd into backup_folder, then you will see a compressed and date-stamped copy of data_folder. To extract the files/directories located in data_folder, you can use tar -xzf ~/backup_folder/data_folder-2024-07-03.tar.gz -C ~/backup_folder.
