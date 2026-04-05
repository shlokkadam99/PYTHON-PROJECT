Simple Python File Manager:

A lightweight, terminal-based file management system built with Python. This utility allows users to interact with their local directory through a simple command-line interface (CLI) to perform basic CRUD (Create, Read, Update, Delete) operations on files.

🚀 Features-

List Directory Contents:Automatically displays all files and folders in the current directory before performing operations.


Create Files: Create new text files and write initial content to them immediately.


Read Files: Open and display the contents of any existing file in the terminal.


Update Files:-
-Rename: Change the name of an existing file.

-Overwrite: Replace the entire content of a file with new data.

-Append: Add new content to the end of an existing file without deleting the old data.

-Delete Files: Remove unwanted files safely from the directory.


🌟 Strategic Advantages-

1. Cross-Platform Compatibility
Because you used the pathlib module, your script handles file paths correctly regardless of whether the user is on Windows (which uses backslashes \) or macOS/Linux (which uses forward slashes /).

Advantage: You don't have to worry about your code breaking when you share it with others on different operating systems.

2. Recursive Visibility
The function path.rglob('*') is a "hidden gem" in your code. Unlike a standard file list, rglob (recursive glob) looks inside every subfolder in your directory.

Advantage: It gives you a "Bird's Eye View" of your entire project structure, making it impossible to lose track of files hidden in deep folders.

3. Data Integrity via "Append" Mode
In the updatefile() function (Option 3), you used the 'a' flag.

Advantage: This allows you to log data or keep a running journal. Unlike the 'w' (write) mode which deletes everything in the file before starting, Append keeps your history safe.

🛠️ How to Use It Effectively
Scenario A: Creating a Structured Project
Instead of just typing a filename like test.txt, you can type data/logs/first_log.txt.

Tip: If the folders data/logs exist, your script will place the file right there, helping you stay organized.

Scenario B: Safe Deletion
The script lists all files with numbers first.

Tip: Always run Option 2 (Read) or check the list in Option 4 (Delete) before confirming. This visual confirmation prevents you from accidentally deleting the wrong main.py or configuration file.

Scenario C: Batch Updating
If you have a file that needs a quick status update:

Select Option 3.

Choose Sub-option 3 (Append).

Type your update (e.g., "Task completed at 5:00 PM").

Result: Your file now acts as a simple, time-stamped ledger.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🛠️ Built With
Python 3.14.3

Pathlib Module: Used for modern object-oriented filesystem path manipulation.

OS Module: Used for system-level file removal.
