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
smbclient -L 10.10.10.1
```
- L: get a list of shares available on a host

SMBMap - view the permissions on the share drives
```
smbmap -H 10.10.10.1
```
- H: IP of host

## WordPress

```
wpscan --url https://machine.htb --disable-tls-checks --api-token <redacted>
```

## GoBuster
```
gobuster dir -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -u 10.10.10.1
```
- dir: uses directory/file enumeration
- w: path to wordlist
- u: url to enumerate
```
gobuster dir -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -u 10.10.10.1 -f
```
- f: appends “/” to each request
```
gobuster dir -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -u 10.10.10.1/cgi-bin/ -x sh,cgi
```
- x: file extensions to search for

## FFuF
```
ffuf -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u http://10.10.44.125/FUZZ
```
```
ffuf -w /usr/share/wordlists/SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.acmeitsupport.thm" -u http://10.10.130.219
```
```
ffuf -w /usr/share/wordlists/SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.acmeitsupport.thm" -u http://10.10.130.219 -fs {size}
```
