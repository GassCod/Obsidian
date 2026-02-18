---
tags:
  - Cyber
  - OffSec
  - pentest_tools
  - web
  - пентест
---
### 📖 Description
`SSH` - is a highly layered protocol that does beyond[^1] simple remote login

**Syntax:**

```bash
ssh {flags} username@host
```


---
> [!NOTE] 🚩 SSH FLAGS
> - `-p` 
> 	Connection on non-standard port (not 22)
> - `-i` 
> 	Specify a specific private key file to use

`Host keys` - a cryptographic "fingerprint" that proves the server's identity to the client
	`~/.ssh/authorized_keys` - Hidden file that contains this host keys

`ssh-keygen` - generates private key

---

### Procedure
1. Adding host key to special file
	- Creating your own key
		```bash
		ssh-keygen
		```
		Main answer for making `authorized key`:
		- Your public key has been saved in /home/gasskali/.ssh/id_ed25519.pub
		

	- `cat yourkey.pub > ~/.ssh/authorized_keys`

---

2. Procedure when web site have own host key:

| Number of action                                        | Action                                | Result                                                                 |
| ------------------------------------------------------- | ------------------------------------- | ---------------------------------------------------------------------- |
| 1. Getting unique host key if we can use [[Identifying and exploring directory traversals]] method | [[Identifying and exploring directory traversals]]                               | We have host key that we can use later                                 |
| 2. Creating host key file                               | `mousepad dt_key`                     | Now we can try to connect to server via ssh using this host key file   |
| 3. Connecting to server by ssh                          | `ssh -i dt_key -p 2222 username@host` | Now if host key correct we have all chances to connect to the server   |

---

## Footnotes

[^1]: Вне/Снаружи
