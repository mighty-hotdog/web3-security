# Cloc

Counts lines of code based on specified criteria and options, then generates printout.  
Useful for:  
- assessing effort during initial project scoping  
- writing final report  

## Installation
In Ubuntu:
```
sudo apt install cloc
```

## Usage
Check out `cloc --help` for the full list of options.  
### Count lines of code in specific directories
```
cloc "./src" "./script"
```
### Generate printout according to specified rules
```
cloc "./src" "./script" --by-file-by-lang --hide-rate
```

### Output to file
```
cloc "./src" "./script" --by-file-by-lang --hide-rate --out=./artifacts/cloc_report
```