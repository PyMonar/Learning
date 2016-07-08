## Learn Python
---
### 1. 基本概念

**数值**类型一共有四种：整数、长整数、浮点数和复数。

**字符串**是一组字符的序列。
- 字符串可以使用单引号也可以使用双引号。
- 三引号表示可以折行的字符串。
- 字符串中的`\`可以表示继续下一行。
- 字符串前增加r或者R表示输入原始字符串。
- 字符串输出unicode则需要前边加u或者U。
- 两个相邻的字符串会被自动连接。

**标识符**首字母必须是字母表中的字母或者下划线`'_'`,标识符对于大小写敏感。python中的变量不需要声明数据类型。

**空白**在python中极其重要！

### 2. 运算符与表达式

`*`操作符可以使字符串重复数次，比如:
```python
# 输出 abcabcabc
print 'abc' * 3 
```

`//`运算符表示取整除。

`<` 运算符可以串接，比如3 < 4 < 5 返回True。

python中表示逻辑运算分别是not、and和or，而非!、&&和||。

python中的bool值为True和False。

### 3. 控制流

**if语句**：
```python
if a == b:
    # do something
elif a > b:
    # do someting
else:
    # do someting
```

**while语句**：
```python
while True:
    # do something
else:
    # do something
```

**for语句**：
```python
for i in range(1, 5): # [1, 5),range可接受第三个参数步长
    # do something
else:
    # do something
```

### 4. 函数

定义函数：
```python
def functionName(a, b = 2):
    ''' This is DocStrings'''
    # do something

# 调用的时候可以设置关键参数
functionName(a = 1, b = 4)
```

### 5. 数据类型

**列表**
```python
# This is my shopping list
shoplist = ['apple', 'mango', 'carrot', 'banana']

print 'I have', len(shoplist),'items to purchase.'

print 'These items are:', # Notice the comma at end of the line
for item in shoplist:
    print item,

print '\nI also have to buy rice.'
shoplist.append('rice')
print 'My shopping list is now', shoplist

print 'I will sort my list now'
shoplist.sort()
print 'Sorted shopping list is', shoplist

print 'The first item I will buy is', shoplist[0]
olditem = shoplist[0]
del shoplist[0]
print 'I bought the', olditem
print 'My shopping list is now', shoplist
```

**元祖**是不可变的列表
```python

zoo = ('wolf', 'elephant', 'penguin')
print 'Number of animals in the zoo is', len(zoo)

new_zoo = ('monkey', 'dolphin', zoo)
print 'Number of animals in the new zoo is', len(new_zoo)
print 'All animals in new zoo are', new_zoo
print 'Animals brought from old zoo are', new_zoo[2]
print 'Last animal brought from old zoo is', new_zoo[2][2]

age = 22
name = 'Swaroop'

print '%s is %d years old' % (name, age)
print 'Why is %s playing with that python?' % name
```

**字典**
```python
# 'ab' is short for 'a'ddress'b'ook

ab = {       'Swaroop'   : 'swaroopch@byteofpython.info',
             'Larry'     : 'larry@wall.org',
             'Matsumoto' : 'matz@ruby-lang.org',
             'Spammer'   : 'spammer@hotmail.com'
     }

print "Swaroop's address is %s" % ab['Swaroop']

# Adding a key/value pair
ab['Guido'] = 'guido@python.org'

# Deleting a key/value pair
del ab['Spammer']

print '\nThere are %d contacts in the address-book\n' % len(ab)
for name, address in ab.items():
    print 'Contact %s at %s' % (name, address)

if 'Guido' in ab: # OR ab.has_key('Guido')
    print "\nGuido's address is %s" % ab['Guido']
```

**序列**
- 序列包括列表、元素和字典
- 序列可以进行索引和切片的操作,切片不更改原序列

切片操作如下例子：
```python
shoplist = ['apple', 'mango', 'carrot', 'banana']

# Slicing on a list
print 'Item 1 to 3 is', shoplist[1:3]
print 'Item 2 to end is', shoplist[2:]
print 'Item 1 to -1 is', shoplist[1:-1]
print 'Item start to end is', shoplist[:]

# Slicing on a string
name = 'swaroop'
print 'characters 1 to 3 is', name[1:3]
print 'characters 2 to end is', name[2:]
print 'characters 1 to -1 is', name[1:-1]
print 'characters start to end is', name[:]
```









