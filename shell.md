## Bash
### Environment
* Check that you are using bash: `echo $BASH`
  * If you are running bash, you will get the path to bash
  
### Commands and Arguments
* The first word is a __command__
* Everything that follows the command is an __argument__
* An argument that starts with a dash is an __option__

### Getting Help
* Manual pages: `man`
  * Move down a page: `space`
  * Move back a page: `b`
  * Search: `/<word to search>`, repeat typing `/` to find the next occurrence
  * Exit: `q`

### File Management
* View file content (dumps file content): `cat <file>`
* View file content and allow browsing: `less <file>`
  * Move down a page: `space`
  * Move back a page: `b`
  * Search: `/<word to search>`, repeat typing `/` to find the next occurrence
  * Exit: `q`
* Initialize the terminal: `reset`
  * Use this for example if you `cat` a binary file and the terminal gets "confused"
* Find out the file type: `file <file>`
* Show the file types of all files in the current directory: `file *`
* Delete a file: `rm <file>`
* Rename file: `mv <file> <new filename>`
* Create multiple directories: `mkdir <directory 1> <directory 2>`
* Move file to a directory: `mv <file> <directory>`
* Delete a non-empty directory: `rm -r <directory>`
* Create a empty file: `touch <file>`
  * If the file exists, a new file is NOT created. Touch modifies the modification and access date.  
#### Opening File in macOS
* Open a file with the default GUI application for the file type: `open <file>`
* Open the current directory in Finder: `open .`
* Choose the application to open the file: `open -a Preview image.jpg`
* Open the directory in VSCode: `open -a 'Visual Studio Code' .`

#### About Filenames
* Filenames can contain just about anything
  * Except `/`
  * Hidden files start with a dot
* Case sensitivity
  * Linux filenames are case sensitive
  * macOS filenames are NOT case sensitive by default
* Extensions are optional
##### Filename Do's and Don'ts
* Use letters, numbers, `-` and `_`
  * If you want to be really safe, don't use uppercase letters
* Try to avoid using spaces
##### Quoting,Escaping,Completion
* __Backslash__ escapes a single character
* __Single quotes__ escapes all characters between them
* Don't use __double quotes__, for now...

#### Paths
* Absolute paths start with a `/`
* Relative paths is resolved relative to the current working directory

#### Copying Files
* List directory content recursively: `ls -R`
* Copy file in a directory to the current directory: `cp <directory>/<file> .`
* Copy and rename: `cp <file> <new filename>`
* Copy multiple files to a directory: `cp <file 1> <file 2> <directory>`
* Copy all files to a directory: `cp * <directory>`

#### Copying Directories
* Copy directory and all its contents: `cp -R <source directory> <destination directory>`
* Copy multiple directories and all its contents: `cp -R <source directory 1> <source directory 2> <destination directory>`
* [macOS] Adding a slash to a directory name ie. `cp -R <director>/ <destination directory>` only copies the directory contents

#### Moving Files
* Move files to another directory: `mv <file 1> <file 2> <destination directory>`
* Move directories to another directory: `mv <directory 1> <directory 2> <destination directory>`

#### Deleting Files