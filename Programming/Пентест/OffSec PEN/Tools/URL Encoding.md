`URL Encoding` - Mechanism for translating special characters into a format that can be safely over the internet within a URL.

**Encoding script**:
```python
python3 -c "import urllib.parse; print(urllib.parse.quote('hello world.', safe=''))"
```

#### Examples:
Space - %20
. - %2