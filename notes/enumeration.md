# Enumeration

Nmap Scripts - FTP
```
ls /usr/share/nmap/scripts/ftp*
```

Nmap Scripts - SSH
```
ls /usr/share/nmap/scripts/ssh*
```

## SMB

SMBClient to access the SMB server
```
smbclient -L 10.10.10.3
```
- L: get a list of shares available on a host

SMBMap - view the permissions on the share drives
```
smbmap -H 10.10.10.3
```
- H: IP of host
