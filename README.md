# Data Structures and Algorithms Project

This project is a **File System Simulator**, built entirely in **C**, that demonstrates the implementation of fundamental **Data Structures and Algorithms**. It provides a command-line interface (CLI) to simulate a hierarchical file system with directories and files, allowing users to execute various file system operations interactively.

## Features

### Core Functionalities
1. **File and Directory Management**
   - **Create**:
     - `mkdir <path>`: Creates a new directory at the specified path.
     - `touch <filename>`: Creates a new file in the current or specified directory.
   - **Read**:
     - `ls <path>`: Lists all files and directories in the specified or current directory.
     - `cat <filename>`: Displays the contents of the specified file.
   - **Update**:
     - `gedit <filename>`: Edits or creates the specified file and updates its content.
   - **Delete**:
     - `rm <filename>`: Deletes the specified file.
     - `rmdir <path>`: Removes the specified directory and its contents.
   - **Navigate**:
     - `cd <path>`: Changes the current working directory to the specified path.
     - `pwd`: Displays the current working directory path.

2. **File System Navigation**
   - Supports both absolute (`/path/to/dir`) and relative (`./path`, `../`) paths.
   - Implements parent-child directory relationships.

3. **Help and Utilities**
   - `help`: Lists all supported commands and their usage.
   - `exit`: Exits the application.

### Technical Highlights
- **Data Structures Used**:
  - **Linked List**: For tokenizing paths during navigation.
  - **Tree Structure**: To represent directories and their hierarchical relationships.
  - **Arrays**: To store files and subdirectories.
- **Algorithms Implemented**:
  - **Binary Search**: For efficient directory and file search.
  - **Sorting**: To maintain directories and files in alphabetical order.

### Constraints
- Maximum of 50 files or subdirectories per directory.
- Root directory (`/`) cannot be modified directly (e.g., creating or deleting files).

## How to Run

### Prerequisites
- A C compiler (e.g., GCC).
- A terminal or command-line interface.

### Steps to Compile and Run
1. Compile the program using:
   ```bash
   gcc -o FileSystemSimulator DSProj.c
   ```
2. Run the executable:
   ```bash
   ./FileSystemSimulator
   ```

## Commands and Usage

Here is a list of all supported commands:

| Command         | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `mkdir <path>`  | Creates a new directory at the specified path.                              |
| `rmdir <path>`  | Removes a directory and its contents from the specified path.               |
| `cd <path>`     | Changes the current working directory to the specified path.                |
| `pwd`           | Displays the current working directory path.                                |
| `ls <path>`     | Lists the contents (files and directories) of the specified directory.      |
| `touch <file>`  | Creates a new file in the current or specified directory.                   |
| `rm <file>`     | Deletes a file from the current or specified directory.                     |
| `cat <file>`    | Displays the content of the specified file.                                 |
| `gedit <file>`  | Edits or creates a file and updates its content.                            |
| `help`          | Displays the list of supported commands with their descriptions.            |
| `exit`          | Exits the application.                                                     |

## Project Structure

- **Directory**:
  - Represents a directory in the file system, containing pointers to its parent, subdirectories, and files.
- **File**:
  - Represents a file in the file system, storing the file name and its content.
- **Path Tokenization**:
  - Splits a given path string into manageable tokens for easier navigation and operation.

## Example Usage

1. Create a directory structure:
   ```bash
   mkdir /home
   mkdir /home/user
   mkdir /home/user/projects
   ```
2. Create and edit files:
   ```bash
   touch /home/user/file.txt
   gedit /home/user/file.txt
   ```
3. View and manage contents:
   ```bash
   ls /home/user
   cat /home/user/file.txt
   rm /home/user/file.txt
   ```
4. Navigate through directories:
   ```bash
   cd /home/user/projects
   pwd
   ```

## Limitations

- Designed as a simulation; does not interact with the actual file system.
- Maximum directory depth and file size are constrained by memory limits.

## Future Enhancements

- Implement persistent storage to save and reload the file system state.
- Add support for advanced commands like `move`, `copy`, and `find`.
- Optimize memory usage and improve error handling.

## Acknowledgements

This project was developed as part of a **Data Structures and Algorithms** course to demonstrate the practical use of data structures in a real-world-like application.

---
