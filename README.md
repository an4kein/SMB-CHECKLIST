# SMB-CHECKLIST

- [Checklist](#checklist)
  - [Enumerate Hostname](#enumerate-hostname)
  - [List Shares](#list-shares)
  - [Check Null Sessions](#check-null-sessions)
  - [Check for Vulnerabilities](#check-for-vulnerabilities)
  - [Overall Scan](#overall-scan)
- [Tools](#tools)

## Checklist

### Enumerate Hostname

`nmblookup -A [ip]`

### List Shares

`smbmap -H [ip/hostname]`

`echo exit | smbclient -L \\\\[ip]`

`nmap --script smb-enum-shares -p 139,445 [ip]`

### Check Null Sessions 

`smbmap -H [ip/hostname]`
    
`rpcclient -U "" -N [ip]`
    
`smbclient \\\\[ip]\\[share name]`

### Check for Vulnerabilities

`nmap --script smb-vuln* -p 139,445 [ip]`

### Overall Scan

`enum4linux -a [ip]`

## Tools

```
nmblookup - collects NetBIOS over TCP/IP client used to lookup NetBIOS names.
smbclient - an ftp-like client to access SMB shares
nmap - general scanner, with scripts
rpcclient - tool to execute client side MS-RPC functions
enum4linux - enumerates various smb functions
wireshark
```


Source: https://0xdf.gitlab.io/2018/12/02/pwk-notes-smb-enumeration-checklist-update1.html
