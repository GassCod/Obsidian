#### SUID Binaries & GTFOBins 

`SUID Binaries` - type of files that always executes with root permissions, rather than with with user permission

How to find all this files on a system:
```bash
find / -perm -u=s -type f 2>/dev/null
```

`find`- To search
`/` - To start from root directory
`-perm -u=s` - look where the user have the SUID bit
`-type f` - look for files onl (not folders)
`2>/dev/null` - hide all "Permission denied" errors

You can find method on bottom in the [GTFOBins](https://gtfobins.org/) website 
`GTFOBins` - that is a list of Unix binaries that can be used to bypass local security  restrictions[^1] in misconfigured systems. 
Main purposes[^2] :
- **Privilege Escalation:** Turning a normal user account into a **root** account
- **Spawning a Shell:** Getting a command prompt from inside a restricted application.
- **File Upload/Download:** Moving files on a system where tools like `wget` or `curl` are blocked.
- **Bypassing Restricted Shells:** Escaping "jails" that limit what commands you can run

##### How you can become root using nmap
1. Run nmap file with `--interactive` flag you can enter to custom nmap console
2. Enter to the regular shell by `!sh`

[^1]: Ограничения

[^2]: Ограничения
