1. Creating and Renaming Files/Directories
In this section, we build a folder structure and manipulate filenames.

Create the directory:
mkdir test_dir
Explanation: This creates a new folder named test_dir in the current location.

Create an empty file:
touch test_dir/example.txt
Explanation: The touch command creates a blank file. We specify the path to place it inside the folder we just made.

Rename the file:
mv test_dir/example.txt test_dir/renamed_example.txt
Explanation: The mv (move) command is used for renaming. It takes the old name as the first argument and the new name as the second.

3. Viewing File Contents
We interact with the system's password file, which is a standard plain-text database.
View full content:
cat /etc/passwd
Explanation: Prints the entire content of the file to the terminal screen.
View first 5 lines:
head -n 5 /etc/passwd
Explanation: The -n flag specifies the number of lines to show from the top.
View last 5 lines:
tail -n 5 /etc/passwd
Explanation: Similar to head, but pulls lines from the bottom of the file.

4. Searching for Patterns
Search for "root":
grep "root" /etc/passwd
Explanation: grep scans the file and filters only the lines that contain the specific string "root".

5. Zipping and Unzipping
This demonstrates how to archive and extract data.
Compress the directory:
zip -r test_dir.zip test_dir
Explanation: The -r (recursive) flag is required when zipping directories to ensure all files inside are included.
Unzip into a new folder:
unzip test_dir.zip -d unzipped_dir
Explanation: The -d flag specifies the destination directory where the files should be extracted.

6. Downloading Files
Download from a URL:
wget https://www.gutenberg.org/files/11/11-0.txt -O sample.txt
Explanation: wget fetches the file from the web. I used a real text file link here (Alice in Wonderland) so the command actually succeeds, and -O renames it to sample.txt.

7. Changing Permissions
Create and lock file:
touch secure.txt && chmod 444 secure.txt
Explanation: chmod 444 sets the permission to read-only (4) for the user, group, and others. The && allows us to run both commands in one line.

8. Working with Environment Variables
Set the variable:
export MY_VAR="Hello, Linux!"
Explanation: The export command makes the variable MY_VAR available to the current shell environment and any child processes.
Verify the variable:
echo $MY_VAR
Explanation: We use the $ prefix to tell the shell to retrieve the value stored inside the variable name.
