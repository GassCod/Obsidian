---
tags:
  - Cyber
  - OffSec
  - pentest_tools
  - пентест
aliases:
  - gobuster
  - pentest
  - pentest_tools
  - offSec
---

### 📖 Description
Instead of crawling[^3] a website by clicking links, `Gobuster` uses a **brute-force**[^broot] approach[^2]. It systematically tests a list of words (from a wordlist) against a target to see what exists.

**Syntax:**

```bash
gobuster {mode} {flags}
```


---
> [!NOTE] 🚩 Gobuster MODES
>- `dir` 
> 	In this mode gobuster works like "link tester" using a brute-force method. It just guess paths based on wordlist given to him.

---

> [!NOTE] 🚩 Gobuster FLAGS
> - `-u`
> 	The target URL gobuster brute-forses
> - `-w`
> 	 The path to your wordlist
> - `-o`
> 	 Saves output to the text file 
> - `-t`
> 	 Limits the quantity of trays




---

### 🧩 Terms
`Brute-force method` — A trial-and-error method used to guess information by systematically trying every possible combination until the correct one is found

`SecList`  —  industry-standard collection of wordlists and payloads[^4] used by security professionals for testing and auditing(Security list)

`Auditing`  — systematic process of inspecting and evaluating[^5] an IT environment to ensure[^6] it is secure, compliant[^7], and functioning correctly

---

### 📂 Useful Paths & Resources

- **Small and fast for quick scans:**
- 
```bash
/usr/share/wordlists/dirb/common.txt
```

- ** The "gold standard" for general web discovery:**
```bash
/usr/share/wordlists/dirb/common.txt
```

- **Part of the SecLists package, containing thousands of specialized lists:**
```bash
/usr/share/wordlists/seclists/Discovery/Web-Content/
```

---

### Additional info:
	Syntax to enumerate dns by gobuster
```shell
gobuster dns -d target.com -w path/to/wordlist
```

Flags:
	`-d` - target domain you want to find subdomains for[^1]

Local directory with wordlists to enumerate DNS
`/usr/share/seclists/Discovery/DNS/` 

The most common: `namelist.txt`


Local wordlist to dir gobuster mode 
`/usr/share/wordlists/dirb/common.txt`

[^1]: Поддомены(Не ебу)

---

### 🧠 Summary

Gobuster used for brute-forcing passwords and  

---
### Other similar tools

[[dirb]], [[ffuf]]

---

## Footnotes
[^broot]: `Brute-force method` — A trial-and-error method used to guess information by systematically trying every possible combination until the correct one is found

[^2]: Подход

[^3]: Сканировать/ползать

[^4]: полезная нагрузка

[^5]: Оценивать

[^6]: Гарантировать

[^7]: Совместимость

[^8]: Quantity - Количество
	
