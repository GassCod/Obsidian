---
tags:
  - Cyber
  - pentest_tools
  - web
---
### 📖 Description
`Curl` is a specific tool for transferring data with URL(It can just download the HTML of the page and  print it to your terminal)
**Syntax:**

```bash
curl https://www.google.com
```


---
> [!NOTE] 🚩  CURL FLAGS (Working With Files)
> - `-o`
> 	Saves the output to a filename you choose
> 	`curl -o filename.html https://example.com`
> - `-O`
> 	Useful for downloading installers or zip files
> - `--data`
> 	Add some information to parameter you entered before =
> 	Specifies data what curl sends
> 	`curl -X POST --data 'Archive=ipconfig' URL

> [!NOTE] 🚩  CURL FLAGS (Inspecting Headers)
> - `-I`
> 	Shows headers of hidden conversations (status code, cookies, server type)
> - `-i`
> 	Do the same but shows headers and page content
> - `-v`
> 	Shows the entire handshake[^1], including SSL certificates and the request you sent.

 >[!NOTE] 🚩  CURL FLAGS (Sending Data(POST))
> - `d`
> 	Sending form data
> 	`curl -d "user=admin&pass=123" https://target.com/login`
> - `-H`
> 	Sending JSON(Usually combines with `-d`)
> 	`curl -H "Content-Type: application/json" -d '{"key":"value"}' https://api.site.com/data`
> - `-X`
> 	Changes method(By default `curl` uses GET or POST methods). Use `-X` for PUT or DELETE
> 	`curl -X DELETE https://api.site.com/user/1`

> [!NOTE] 🚩  CURL FLAGS (Handling[^2] Security and Cookies)
> - `-k`
> 	Ignore SSL[^3] errors 
> 	`curl -k https://10.10.10.15`
> - `-u`
> 	For sites protected by Basic Auth(Sites with row login and password fields)
> 	`curl -u username:password https://protected-site.com`


---

## Footnotes

[^1]: Процесс установления соединения

[^2]: Обработка

[^3]: SSL (Security Socket Layer) - errors occurs[^4] when web browser cannot establish[^5] a secure connection with website
	
	
	[^4]: Происходит
	
	[^5]: Установить
	
	
	
