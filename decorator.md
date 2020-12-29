# Decorator
## what is decorator
a closure that adds additional functionality for function  
***if this closure has only one paramter and it is function, this closure is decoratot***
## features
1. did not modify original function
2. did not modify how original function is used
3. add additional functionality to the original function

## example usage
log output,
timer

```python
def decorator(funv):
    def inner(*args, **kwargs):
        begin=time.time
        result = func(*args, **kwargs)
        end=time.time
        result = end - begin
        print("this function uses ", result)
        return result
    return inner

@decoratot
def add(*args, **kwargs):
    result = 0
    for value in args:
        result += value
    for value in kwargs.values():
        result += value
    return result

result = add(1, 2)
```

# class decorator
```python
class MyDecorator(obj):
    def __init__(self, func): # __init__ is needed when use decorator
        self.__func = func   # __ means the attributes is private

    def __call__(self, **args, **kwargs):
        print("课讲完了")
        self.__func()

@MyDecorator  #  ==> show = MyDecorator(show),  which is to init a class, thus need a __init__ inside the class
def show():
    print("快要下学了")

show()  # show is a instant of MyDecorator, thus show() will excute __call__ in the class, if no __call__ method, will raise exception
```