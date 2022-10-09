Initial Scan:
```
nmap -sC -sV -O -oA initial 10.10.10.4
```
- sC: run default nmap scripts
- sV: detect service version
- O: detect OS
- oA: output all formats and store in file initial

UDP Scan:
```
nmap -sU -O -p- -oA udp 10.10.10.4
```
- sU: udp scan
- O: detect OS
- p: scans all ports
- oA: output all formats and store in file udp

Full Scan:
```
nmap -T4 -A -p- -oA full 10.10.10.4
```
- T4: aggressive timing template
- A: enable OS detection, version detection, script scanning, and traceroute
- p: scans all ports
- oA: output all formats and store in file full
