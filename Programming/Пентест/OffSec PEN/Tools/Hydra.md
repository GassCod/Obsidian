---
tags:
  - Templates
---
### 📖 Description

Hydra is using to crack passwords and logins

**Syntax:**

```bash
hydra {flags} {wordlists if flags requiers} {target ip} {service}
```


---
> [!NOTE] 🚩 Hydra FLAGS
> - `-l`
> 	Use specific username
> - `-L`
> 	Use list of usernames from a file
> - `-p`
> 	Use a specific password
>- `-P`
>	Use a wordlist of passwords
>- `-vV`
>	Show every attempt as it happens
>- `-s [port]`
>	For run hydra on non-standart ports
>- `-t` 
>	How many tasks are running in parallel(Default 16)


---
#### Types of services
1. `ssh`:
	```
	ssh
	```
2. Web login:
	```
	http-form-post "/login.php:user=^USER^&pass=^PASS^:F=Login failed"
	```
	
	`^USER^` - placeholder for login
	`^PASS^` - placeholder for password
	`F=` - text on the page on wrong attempt
---
### 🧩 Terms


---

### 📂 Useful Paths & Resources


---

### 🧠 Summary

---

## Footnotes
