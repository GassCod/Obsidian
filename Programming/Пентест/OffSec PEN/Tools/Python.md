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
> - `-c`
> 	Execute command after flag


---
>[!INFO] PYTHON SCRIPTS
>- `http.server`
>	Library to start a web server on your kali
>- `pty`/ `inmport pty`/ `pty.spawn(/bin/bash)`
>	Creates virtual terminal devise and new shell inside it


---
### All scripts i use(At the moment of writing)
When you are connected to reverse shell it is the regular TTY shell that doesnt supports some commands like su. 
`pty` - changes TTY terminal into normal one(u can use most commands)

```python
python -c `import pty;pty.start("/bin/bash")`
```


[[Programming 1/Пентест/OffSec PEN/Tools/Decryption]]:
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

[[Programming 1/Пентест/OffSec PEN/Tools/URL Encoding]]:
```python
python3 -c "import urllib.parse; print(urllib.parse.quote('hello world.', safe=''))"
```

[[Programming 1/Пентест/OffSec PEN/Pentest methods/Remote File Inlusion(RFI)|Starting web server on our kali]]
```python
python3 -m http.server 80
```
>[!TIP]
>You can check your actual ip address by console command: `ip addr`
---

