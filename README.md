Download Link: https://assignmentchef.com/product/solved-solvedmerge-sourcedirectory1-sourcedirectory2-destinationdirectory-script-solution
<br>
Write a python script that will implement the following command:

merge sourcedirectory1 sourcedirectory2 destinationdirectory

The idea is that the contents of sourcedirectory1 and sourcedirectory2 are going to be copied and merged together into a new destination directory. The destination directory should be created using mkdir() to hold the copied data. The original contents of the two source directories will not be altered. Your script should first parse the command’s arguments to see if there are any errors such as invalid names, missing or extra directory names, file names rather than directory names, two names that are the same, or a destination directory that already exists.

The merger is a union operation, so that if a file/directory exists in either source directory it is included in the new directory. Whenever a file exists in both source directories, the newer version of the file should be copied. You can use the os.path.getmtime() function to see when a file was last modified. If two items that have the same name are not both a file or both a directory, then an error message should be displayed saying that you are skipping this pair of incompatible objects. If the two items with the same name are both directories, then you should call your merging routine recursively to process these subdirectories. If one or both of the items is a symbolic link, you should look at the properties of the item being linked to rather than the link itself. You should also end up copying the linked item rather than the link itself.

You should not use the copytree() function in the shutil library in this program. You should write your own recursive function to copy a directory and its contents if needed. When copying a file, use the copy2() function in the shutil library, rather than the copy() function we discussed. This version will preserve as much meta information about the file as possible, such as permissions and times. Make sure that you create new functions appropriately now that you know how.

Submit your source code. Submit the results of your program by showing detailed directory listings (including file times) of two source directories and a newly created destination directory.