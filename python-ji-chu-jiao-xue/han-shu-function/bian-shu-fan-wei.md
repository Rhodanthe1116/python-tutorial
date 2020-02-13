# 變數範圍 Scope

變數可以區分成 **全域 Global** 和 **區域 Local**，一般我們之前在函數外使用的都是全域變數，在程式的任何地方都可以任意使用

```python
spam = "global spam"
print(spam)
if True:
    print(spam)
```

```python
if True:
    spam = "global spam"
    print(spam)
print(spam)
```

但是到了函數裡面就不一樣了：

```python
def scope_test():
    spam = "local spam"
    print(spam)
   
scope_test() 
print(spam)
```

會出錯

```python
local spam
Traceback (most recent call last):
  File "C:\Users\hwww\Desktop\ff.py", line 6, in <module>
    print(spam)
NameError: name 'spam' is not defined
```

第二行**在函數中的指定`=`會產生區域變數**，區域變數只能在相同函數內使用，也就是說只能在`scope_test()`裡面使用，若是到了函數外面，在主程式區使用，便會不知道此變數是什麼。

以下是一個同時使用了全域變數跟區域變數的範例，可以清楚的看到取用的情況，**函數內會優先取用最內層的區域變數**。

```python
def scope_test():
    spam = "local spam"
    print(spam)
   
spam = "global spam"
print(spam)
scope_test() 
```

但若是我們需要在函數裡面使用全域變數，需要使用 **global** 語法，來使函數中的變數成為已經宣告的全域變數。

```python
def scope_test():
    global spam
    print(spam)
   
spam = "global spam"
print(spam)
scope_test() 
```

其實只要不要在函數中使用`=`，就不會產生區域變數，因為**在函數中的指定`=`會產生區域變數**。不使用`=`，變數會自動變成全域變數，如下：

```python
def scope_test():
    print(spam)
   
spam = "global spam"
print(spam)
scope_test() 
```

`global`跟`=`不能放在一起同時使用，因為`global`會使該變數是全域，而`=`會是該變數是區域，兩者衝突，需要分開使用。

```python
def scope_test():
    global spam
    spam = "changed global spam"
    print(spam)
   
spam = "global spam"
print(spam)
scope_test()
print(spam)
```



