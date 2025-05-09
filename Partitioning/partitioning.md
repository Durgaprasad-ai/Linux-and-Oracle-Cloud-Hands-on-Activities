# 1. What is Partitioning ? Types of Partitioning ?
Ans > Partitioning in linux refers to dividing a larger storage device into smaller chunks known as partitions. Each partition behaves like an individual disk, which can be formatted with file systems to store system files, user files and swap space.

# Benefits of Partitioning :

 > **Improved system Organization :**  Different types of data like system files, user files, logs can be stored in the seperate partitions, which helps in managing filesystems easier.

> **Enhanced Security :** you can set different permissions and access controls per partition. For example, you can restrict the executable files for /home, /tmp from running which reduces the vulnerabilities to malware.

> **Better Data Protection :** If one partition is corrupted, then it will not effect the partitions which minizes the data loss.

> **Easier Backup and Restoration :** You can take backup for each partition individually , no need to take backup for whole system.


# Types of Partitioning :

> **Master Boot Record ( MBR ) :**

	- Stores boot and partition information in the first 512 bytes of disk.
	- Allows to create only four primary partitions. 
	- If you want to create more than four , then one of primary partition will be converted into extended partition.
	- Under extended partition , you can create as many logical partitions as you want.
	- Its critical drawback is that it only supports disks until 2TB.
	- fdisk command is used to partition disks.

> **GUID Partition Table ( GPT ) :**
	
	- stores boot and partition information at different places across the disk.
	- Allows to create 128 primary partitions.
	- Each partition is assigned with GUID ( Globally Unique Identifier ) ensuring no two partitions have same identity.
	- GPT supports disks larger than 2TB.
	- gdisk command is used to partition disks.

