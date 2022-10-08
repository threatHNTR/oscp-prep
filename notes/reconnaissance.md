# Reconnaissance

## Nmap

Initial Scan:
- sC: run default nmap scripts
- sV: detect service version
- O: detect OS
- oA: output all formats and store in file initial

```
nmap -sC -sV -O -oA initial 10.10.10.4
```

Full Scan:
- T4:
- A:
- p:
- oA: output all formats and store in file full

```
nmap -T4 -A -p-  -oA full 10.10.10.4
```
