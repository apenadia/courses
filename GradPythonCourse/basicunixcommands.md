# Understanding Basic Unix Commands

# What is *nix
* UNIX is an operating system developed int he 1960's
* UNIX has proven to be a reliable multi-user and multi-tasking system
* There are different types of UNIX
  * Sun Solaris
  * GNU/ **Linux**
  * MacOS X

# Basics of the Operating System
* **The Kernel**
  * Essentially the "Hub"
  * Works with **The Shell** by managing the filestore/communications involved in system calls
* **The Shell**
  * Serves as an interface between the user and the kernel
  * The Shell is a Command Line Interpreter (CLI)
  * Essentially, it will understand commands and carry out their function

# Directories
## Finding where files are kept
* The file system is arranged in a hierachial structure
* / is the **root** directory
* /bin is a subdirectory of the root directory that contains programs that are necessary for the most basic functions of the system (ie. starting and repairing the system)
* /usr is also a subdirectory of the root directory that can be broken down into two sub categories
  * /usr/bin are programs run by users and are necessary for the functions of the system
  * `/usr/local/bin` are where installed programs by the user are stored

# Basic Commands
* **ls**
 * Lists files in your current working directory
 * Exception: Unless you are very familiary with Unix, some files should not be changed and are kept hidden
 * These files begin with a period (.)
 * To find all files, use the **ls -a** command: for example,
 ```
 # ls -a
 .
 ..
 .hidden_file
 something_else.txt
 ```
* **mkdir**
 * Allows you to make a subdirectory in your home directory
 * Example: % mkdir PoonLab
* **cd**
 * Allows you to change directory from the current working directory
 * Example: % cd PoonLab

* **(.)**
 * The current directory
 * Example: % cd .
* **(..)**
 * Considering the hierachal structure of the files, the parent directory command will bring you directly up the hierarchy
* **pwd**
 * Present working directory
 * Will give the full pathname of the current directory that you are in

* **cp**
 * Allows you to copy files
 * Example: cp file file1 allows you to copy file in your current working directory and name it file1
* **mv**
 * Allows you to move files
 * Example: mv file file1 allows you to move file to file1
* **rm** and **rmdir**
 * Allows you to remove a file (rm) or remove a directory (rmdir)

# Access Rights to Directories and Files
* Each file has access rights associated with it
* These right can be found using the **ls -l** command, which essentially gives you the "long" listing of the file name
* Example: 
  ```
  -rwxrw-r-- 1 echadwi 562 Dec 2nd 2016 PoonLab
  ```
 * The 9 letter symbol at the beginning gives the access rights
* Access rights on files
 * **r**
  * Read permission
 * **w**
  * write permission
 * **x**
  * execution permission
* Access rights on directories
 * **r**
  * Allows users to list files in directory
 * **w**
  * Allows users to delete or move files
 * **x**
  * Allows users the right to access files in directory

# Changing Access Rights to Directories and Files
* **chmod**
 * Allows owner to change permissions of a file
 * Options:
  * **u** user
  * **g** group
  * **o** other
  * **a** all
  * **r** read
  * **w** write and delete
  * **x** execute and access directory
  * **+** add permission
  * **-** remove permission
 