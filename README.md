# Linux-Learning-Journey---Week-3
Linux File Management, Backup and File Analysis

Introduction

During Week 3, I studied Linux file management, filesystem navigation, directory structures, file operations, archiving, compression, and viewing file contents from the terminal.

The Linux filesystem uses a unified hierarchical structure that begins at the root directory /. The Command Line Interface (CLI) provides a fast and controlled way to manage files and directories. The home directory can be represented using the ~ shortcut.

1. Linux Filesystem and Directory Structure

Linux organizes files within a hierarchical filesystem structure.

The root directory is represented by:

/

The tilde character represents the current user's home directory:

~

The CLI allows users to navigate and manage files using commands.

2. Navigating the Filesystem
pwd

The pwd command displays the user's exact current location in the filesystem.

pwd
cd

The cd command is used to change directories.

Running cd without an argument returns the user to the home directory.

cd
Absolute Paths

An absolute path specifies the exact location of a directory and begins at the root directory.

Example:

/home/sysadmin
Relative Paths

A relative path begins from the user's current directory rather than from the root of the filesystem.

3. Directory Shortcuts

Linux provides special characters for navigating directories.

Current Directory: .

The single dot represents the current directory.

.
Parent Directory: ..

The two dots represent the parent directory, which is one level above the current directory.

..

These shortcuts make navigating the filesystem easier.

4. Listing Files and Directories

The ls command is used to view directory contents.

ls
Hidden Files

The -a option displays all files, including hidden files.

ls -a
Long Listing

The -l option provides detailed information about files, including:

File type
Permissions
Link count
Ownership
File size
Modification timestamp
ls -l
Human-Readable File Sizes

The -h option displays file sizes in units such as KB, MB, and GB.

ls -lh
Listing a Directory Itself

The -d option can be used to list the directory itself rather than its contents.

ls -ld




5. Copying Files and Directories

The cp command is used to copy files.

The basic structure is:

cp source destination

A source and destination are required.

Example:

cp file.txt backup.txt
Verbose Mode

The -v option means verbose. It causes cp to display output when the operation is successful.

cp -v file.txt backup.txt
Copying Directories

The -r option allows cp to copy directories and their contents recursively.

cp -r source_directory destination_directory
Preventing Overwriting

The -i option makes cp ask for confirmation before overwriting an existing file.

cp -i file.txt backup.txt

The -n option prevents existing destination files from being overwritten.

cp -n file.txt backup.txt

These options provide additional control and help prevent accidental data loss.

6. Moving and Renaming Files

The mv command is used to move files and directories or rename them.

Basic syntax:

mv source destination
Moving a File
mv file.txt documents/
Renaming a File
mv oldname.txt newname.txt

If the destination is a directory, the file is moved into that directory.

Useful mv options include:

mv -i

Prompts before overwriting a file.

mv -n

Prevents overwriting the destination.

mv -v

Displays information about the resulting move.

7. Creating and Removing Files
touch

The touch command is used to create a file.

touch notes.txt
rm

The rm command removes files.

rm notes.txt

The -i option can be used to request confirmation before deletion.

rm -i notes.txt

This is particularly useful when deleting multiple files because it gives the user an opportunity to confirm each deletion.

8. Creating Archives with tar

The tar command, short for Tape Archive, combines several files into a single archive file.

This makes it possible to package multiple files together and later extract them.

Create an Archive

The create mode is represented by -c.

tar -c -f archive.tar file1 file2
List Archive Contents

The -t mode displays the contents of an archive without extracting it.

tar -t -f archive.tar
Extract an Archive

The -x mode extracts files from an archive.

tar -x -f archive.tar

The three main tar operations studied were:

-c for creating an archive
-t for listing archive contents
-x for extracting files
9. ZIP Archives

The zip command creates compressed ZIP archives.

zip archive.zip file.txt

The -r option recursively includes subdirectories.

zip -r archive.zip directory/
Extracting ZIP Archives

The unzip command extracts files from a ZIP archive.

unzip archive.zip

The -l option lists the files contained in a ZIP archive without extracting them.

unzip -l archive.zip




10. Viewing File Contents

Linux provides commands for displaying the contents of text files directly in the terminal.

cat

The cat command can display text file contents and can also be used to combine copies of text files.

cat notes.txt
less

The less command is a pager that displays large amounts of text one page at a time.

It is also the default pager used by commands such as man.

less largefile.txt
more

The more command is another pager for viewing text one page at a time. The course material notes that it has fewer features than less and is available across Linux distributions.

Key Commands Learned
Command	Purpose
pwd	Display the current directory
cd	Change directory
ls	List directory contents
cp	Copy files and directories
mv	Move or rename files
touch	Create a file
rm	Remove files
tar	Create, list, and extract archives
zip	Create compressed ZIP archives
unzip	Extract ZIP archives
cat	Display file contents
less	View files one page at a time
more	View files one page at a time
Key Options Learned
Option	Command	Purpose
-a	ls	Show hidden files
-l	ls	Show detailed information
-h	ls	Show human-readable sizes
-d	ls	List the directory itself
-r	cp	Copy directories recursively
-v	cp / mv	Display operation details
-i	cp / mv / rm	Prompt for confirmation
-n	cp / mv	Prevent overwriting
-c	tar	Create an archive
-t	tar	List archive contents
-x	tar	Extract an archive
Week 3 Reflection

Week 3 helped me develop practical skills for managing files and directories through the Linux command line.

I learned how to navigate the filesystem using absolute and relative paths, inspect directory contents, work with hidden files, and view detailed file information.

I also practiced copying, moving, renaming, creating, and removing files. The use of options such as -i and -n showed me how Linux commands can provide additional protection against accidental overwriting or deletion.

Finally, I learned how tar, zip, and unzip can be used to organize and manage archives, as well as how cat, less, and more can be used to inspect file contents.

Week 3 Summary

Week 3 focused on Linux file management, backup and archiving, filesystem navigation, and file analysis from the terminal.

The skills developed during this week provide an important foundation for building a Linux file-management and backup utility using Bash.
