# Aderyn

Static analyzer for `Solidity`. Written in `Rust`.  
https://github.com/Cyfrin/aderyn  
https://support.cyfrin.io/en/collections/11474635-aderyn  

## How it works
Very similiar to Slither.

Runs a suite of detectors that:  
- goes through the code fed to it,  
- picks up vulnerabilities,  
- generates a printout about them and where they are found in the code.  

Also provides a framework for writing custom detectors.  

## Installation
Recommended to install via `Cyfrinup`. This tool installs 2 tools developed and distributed by Cyfrin:  
- Aderyn - a static analyzer for Solidity  
- Safe-Hash - a Safe wallet transaction verification tool  

Install Cyfrinup 1st.  
```
curl -L https://raw.githubusercontent.com/Cyfrin/up/main/install | bash
```
Then run `Cyfrinup` to install both tools.  
```
cyfrinup
```

## Usage
1st compile all sourcecode, then run Aderyn on them.  
Aderyn looks at the code as well as their dependencies.  
Learn about the various options and functionalities available in the Aderyn docs. https://support.cyfrin.io/en/collections/11474635-aderyn  

### Run in project directory
Run Aderyn in the project root directory to parse the whole codebase.  
```
cd <project-directory>
aderyn .
```

### Run in specific directories
Use `-i` or `--include` to explicitly specify which directories (child directories included) Aderyn is to look into.  
```
aderyn -i src/abstract/,src/interfaces/,src/protocol/
```

### Output to a file
```
aderyn . -o ./artifacts/aderyn_report.md
```