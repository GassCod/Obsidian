---
создал заметку: "{{date}}"
tags:
  - "#Cyber"
  - "#OffSec"
  - "#пентест"
  - "#pentest_tools"
aliases:
  - nmap
  - pentest_tools
  - pentest
  - offSec
---

### 📖 Description

`nmap` is a tool used to identify open ports and the services running on them.  
It sends a series of probes to determine which ports are open and what exactly is running behind them.

**Syntax:**

```bash
nmap <flags> {target-ip}
```

— Run `nmap` against a target IP using the specified flags ⬇️

---
> [!NOTE] 🚩 Nmap FLAGS
> 
> - `-sV`  
>     Instead of only detecting open ports, this flag probes services to determine what is running on a port
>   
> - `-p {port}`  
>     Specifies the port number to scan
>     
> - `--script=https-enum`
>     Runs a script designed to discover hidden directories and files
> - `--script http-wordpress-enum`
> 	 This script scans target to wordpress plagin
> - `--script=ssh-brute`  
>     Performs a brute-force attack to obtain an SSH password
>     
>  - `--script "{name of NSE script}"`
> 	 Run a NSE script from that you named from local NSE scripts db
>- `--script-updatedb`
>	 Update script database index that Nmap uses to track all available NSE scripts


---
### 🧩 Terms

- `CVE` — Common Vulnerabilities and Exposures[^1]
    
- `NSE` — Nmap Scripting Engine
    

---

### 📂 Useful Paths & Resources

- **Local NSE scripts location:**
    

```bash
/usr/share/nmap/scripts
```


- **Official NSE scripts documentation:**
    [https://nmap.org/nsedoc/scripts/](https://nmap.org/nsedoc/scripts/)
    

---

### 🧠 Summary

In general, `nmap` is used when searching for vulnerabilities in web servers and other network services.

---

## Footnotes

[^1]: Воздействия 