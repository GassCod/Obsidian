## Basic Syntax

```bash
grep [option] pattern [file]
```

**Flags:**
- `-r` - Recursive
- `*` - represents(print) every file in current directory | This flag usable for every similar to cat commands 

Grep finds files and directories by the pattern

You can find files into directory by recursive[^1] searching. For example:
```shell
grep -R . "We can pu dir here but if no we will just do it in this dir"
```

or you can search into exact file:
```shell
grep "Hello" file.txt
```

[^1]: Повторения 
	
