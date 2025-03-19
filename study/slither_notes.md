# Slither

Static-analysis tool for `Solidity` and `Vyper`. Written in `Python3`.  
https://github.com/crytic/slither  

## How it works
Runs a (rather comprehensive and ever-growing) suite of detectors that:  
- goes through the code fed to it,  
- picks up vulnerabilities,  
- generates a printout about them and where they are found in the code.  

Slither provides an API for writing custom detectors.  

## Installation
### Python3
Slither requires `Python3` (v3.8 and later) to install and to run.
```
sudo apt install python3
```

### pipx
One way to install Slither is by using `pipx`. This is a tool for installing and running `Python` applications  
in isolated environments that do not pollute the global `Python` environment or cause dependency conflicts.  
```
python3 -m pipx install slither-analyzer
```
or
```
python3 -m pipx install slither-analyzer --force
```
`pipx` creates a virtual environment in `~/.local/share/pipx/venvs/`, installs `slither-analyzer` and all its  
dependencies, and links the executable (ie: `slither`) to `~/.local/bin/` via a symlink.  

When `slither` is run, it runs in the virtual environment.


## Usage
### Run in project directory
Run Slither in the project directory to parse the whole project codebase.  
This is the ideal method, allowing Slither to look at the dependencies as well as the project code itself.  
```
cd <project-directory>
slither .
```

### Run on single files
Slither may also be run on a single file.  
```
slither src/tokenswap.sol
```

### Configuration
Slither may also be run with a set of config options specified in the file `slither.config.json`.  
```
slither . --config-file slither.config.json
```

Sample `slither.config.json`.  
```
{
    "detectors_to_exclude": "naming-convention,solc-version,similar-names",
    "exclude_informational": false,
    "exclude_low": false,
    "exclude_medium": false,
    "exclude_high": false,
    "disable_color": false,
    "filter_paths": "(mocks/|test/|script/|upgradedProtocol/)",
    "legacy_ast": false,
    "exclude_dependencies": true
}
```

### Output report to file
The `--checklist` switch instructs Slither to generate a markdown doc with the detector output.  
This doc can be output to a file using `> ./output-directory-name/slither-report-name.md`.  
```
slither . --config-file slither.config.json --checklist > ./artifacts/slither_report.md
```
