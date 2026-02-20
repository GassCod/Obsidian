---
tags:
  - Templates
---
### 📖 Description

John is using to offline crack passwords

**Syntax:**

```bash
john [hash file] [flags/options]
```


---
> [!NOTE] 🚩 JOHN FLAGS
> - `--wordlist=[file]`
> 	Path to wordlist u use to brute force password
> - `--format=[format]`
> 	hash format(You can use [[hash-identifier]] to get file hash type)
> 	Exampe: `Raw-MD5`
> - `--rules=none`
> 	disables all rules(Used to avoid the capitalization problem)


---
### 🧩 Useful features

If you have `.zip`, `.pdf`, `ssh key` you can use "tojohn" tool to extract the hash first:
	zip - `zip2john secret.zip > hash.txt`
	SSH Keys - `ssh2john id_rsa > hash.txt`
	PDF - `pdf2john document.pgf > hash.txt`


---

### 📂 Useful Paths & Resources


---

### 🧠 Summary

---

## Footnotes
