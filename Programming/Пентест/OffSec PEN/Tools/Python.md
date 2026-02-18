---
tags:
  - pentest_tools
  - Console
  - programming_language
  - Templates
---
### 📖 Description
`Python` is a so big library with many useful functions using in pentest

**Syntax:**

```bash
python3 {flags} {script name/script}
```


---
> [!NOTE] 🚩 PYTHON FLAGS
> - `-m`  (Module)
> 	This flag tells Python to search its internal library for a specific script and run it as a "main" program
> 


---
>[!INFO] PYTHON SCRIPTS
>- `http.server`
>	Library to start a web server on your kali


---
### All scripts i use(At the moment of writing)
[[Decryption]]:
```python
import base64

data = "Vm0wd2QyUXlVWGxWV0d4WFlUSjRWbJl3Wkc5V2JHeDBaTV..." # Your long string

while True:
    try:
        # Try to decode
        data = base64.b64decode(data).decode('utf-8')
    except Exception:
        # If it fails, we've reached the actual flag!
        print(f"Final Result: {data}")
        break
```

[[URL Encoding]]:
```python
python3 -c "import urllib.parse; print(urllib.parse.quote('hello world.', safe=''))"
```

[[Remote File Inlusion(RFI)|Starting web server on our kali]]
```python
python3 -m http.server 80
```
>[!TIP]
>You can check your actual ip address by console command: `ip addr`
---

