## Syntax
```shell
echo {some encrypted string} | base{number of base following table} -d 
```


`echo` - this shit is used to translate some string u write into console to machine code or easier it just helps to computer recognize string for example some sipher[^2] you wrote

[[Json Web Tokens| One mor decription method]] - encoding to JWT tokens(usually in cookies)

| **Encoding**             | **Identifying Features**                                                    | **Common Use**                                          |
| ------------------------ | --------------------------------------------------------------------------- | ------------------------------------------------------- |
| **Base16 (Hex)**         | Only numbers (0-9) and letters (A-F). Often starts with `0x`.               | Every day in CTFs. Usually looks like: `48 65 6c 6c 6f` |
| **Base32**               | All uppercase letters (A-Z) and numbers 2-7. Lots of `=` padding.           | Used when systems are case-insensitive.                 |
| **Base58**               | Like Base64 but removes "confusing" characters like `0`, `O`, `I`, and `l`. | Common in Bitcoin/Crypto challenges.                    |
| **Base85**               | Uses almost every symbol on the keyboard (e.g., `<~...~>`).                 | Extremely dense; used in Adobe PDF or Git files.        |
| **Base64**, most popular | `A-Z`, `a-z`, `0-9`, `+`, `/`, and `=` padding.                             | `SGVsbG8=`                                              |
|                          |                                                                             |                                                         |

`Base64` - this is way to represent binary data(more info in the table above[^1])

`-d` - this flag to `base` instruments family means decode

>[!ATTENTION]
> You could have encrypted data in your ctf challenge like matrioshka.
> This matrioshka means that you may do this base64 decryption more than 1 time
> Or use python scrtpt

Like this:
```shell
echo "..." | base64 -d | base64 -d | base64 -d ...
```

Python script:
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





[^1]: Выше
	

[^2]: Шифр
	
