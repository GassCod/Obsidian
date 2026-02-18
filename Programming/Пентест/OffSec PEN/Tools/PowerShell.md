---
tags:
  - Cyber
  - OffSec
  - pentest_tools
  - programming_language
---

#### Entering to powershell from linux
```bash
pwsh
```

---
>[!INFO] POWERSHELL FLAGS
>- `-enc`
>	To add base64 encoded string to `powershell`

>[!INFO]
>If you want to use powershell code you need to put `powershell ` parameter after `cmd=`


---
#### Creating file
```powershell
$Text = '...'
```

---
#### Encoding file
```powershell
$Bytes = [System.Text.Encoding]::Unicode.GetBytes($Text)
```

---
#### Making base64 file from encoded version
```powershell
$EncodedText =[Convert]::ToBase64String($Bytes)
```