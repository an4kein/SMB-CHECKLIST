# SMB-CHECKLIST

- [Checklist](#checklist)
  - [Enumerate Hostname](#enumerate-hostname)
  - [List Shares](#list-shares)

### Checklist

#### Enumerate Hostname

`nmblookup -A [ip]`

#### List Shares

`smbmap -H [ip/hostname]`
`echo exit | smbclient -L \\\\[ip]`
`nmap --script smb-enum-shares -p 139,445 [ip]`



Source: https://0xdf.gitlab.io/2018/12/02/pwk-notes-smb-enumeration-checklist-update1.html
