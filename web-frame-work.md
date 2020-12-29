# Web Framework:

## Framework Flow
![alt text](./res/web_framework_flow.PNG)

## router
use decorator to manage/add router

```python
def route(path):
    def decorator(func):
        route_list.append((path, func))
        def inner():
            result = func()
            return result
        return inner
    return decorator
```