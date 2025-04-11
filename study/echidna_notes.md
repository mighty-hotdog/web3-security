# Echidna

Fuzzing tool for `Solidity`. Written in `Haskell`.  
https://github.com/crytic/echidna  
https://github.com/crytic/building-secure-contracts/tree/master/program-analysis/echidna  
https://github.com/trailofbits/eth-security-toolbox  

## How it works  

## Quickstart
Recommended to just spin up a `Docker` image with `Echidna` preinstalled.  
Crytic the developer and maintainer of `Echidna` offers its own version.  
```
$ docker run --rm -it -v `pwd`:/src ghcr.io/crytic/echidna/echidna
```

Trail of Bits offers an alternative which includes several other tools: `Slither`, `Medusa`,  
`solc-select`, `Foundry`, `Vyper`, `n`, `npm` and `Yarn`, and `Python`.  
`/xyz` is the local directory you wish to grant the `Docker` container access to.  

```
docker run -it -v "$PWD":/xyz trailofbits/eth-security-toolbox
```

## Other Usage Options

## Configuration

## Output report to file
