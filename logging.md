# logging
## why logging
1. 
2.
3.

## logging Level
1. DEBUG
2. INFO
3. WARNING
4. ERROR
5. CRITICAL

usually use 2,3,4, default 3， change using
```python
logging.basicConfig(level=logging.DEBUG,
                    format="%(asctime)s-%(filename)s[lineno:%(lineno)d]",
                    filename="log.txt",
                    filemode="a")
```
