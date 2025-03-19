# Tree

Creates a tree printout of files and directories based on specified criteria and options.  
Useful for:  
- picking out and generating list of directories and files during initial project scoping  
- writing final report  

## Installation
Can be installed in Ubuntu using `snap` or the standard `apt install`.  
Installing via `snap` gives a later, more up-to-date version of `tree` for some reason.  
```
sudo snap install tree
```
or
```
sudo apt install tree
```

## Usage
### Run `tree` on specific directories
```
tree ./src/ ./scripts/
```

### Output to file
```
tree ./src/ ./scripts/ > scope.txt
```