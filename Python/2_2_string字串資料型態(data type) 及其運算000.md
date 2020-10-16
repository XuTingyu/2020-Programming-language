# 眾多資料型態(data Type)及其各種運算
    >* 數值(Numeric)資料及其運算
    >* 字串(string)及其運算
    >* 列表(list)資料及其運算
    >* 字典(dict)資料及其運算  
    >*[自我練習]tuple資料及其運算  
    >*[自我練習]set資料及其運算 
    
```
 本課程規劃讓同學快速掌握python程式的開發技術
 還有更多技術及細節 請務必閱讀更多教材深入
```

```
from queue import Queue
q = Queue()
q.put(1)
q.put(2)
q.put(3)
q
print(q.queue)

q.get()
 ```
 
### 快速入門 
```
數值(Numeric)資料及其運算

a = 17 / 3
b = 17 // 3
c = 17 % 3

a,b,c
```
```
字串(string)及其運算

var1 = 'Hello Python!'
 
print("var1[0]: ", var1[0])
print("var1[1:8]: ", var1[1:8])

變數值以一對雙引號 (「"」)或單引號 (「'」)
存取字串中的值: 使用方括號
```
```
列表(list)資料及其運算


list1 = [21, 33, 14, 12, 32,98]

list1[1]
len(list1)
max(list1)
min(list1)
sum(list1)

list是Python中最基本的資料結構。
創建一個list，只要把逗號分隔的不同的資料項目使用方括號括起來即可
list中的每個元素都分配一個數字(位置|索引)，第一個索引是0，第二個索引是1，依此類推。
list都可以進行的操作包括索引，切片，加，乘，檢查成員。
Python已經內置確定list的長度以及確定最大和最小的元素的方法。
```
```
字典(dict)資料及其運算 
 
dict = {'Name': 'DaDaLong', 'Age': 17, 'Class': 'First'}
 
print("dict['Name']: ", dict['Name'])
print("dict['Age']: ", dict['Age'])

字典的每個鍵值(key=>value)對  用冒號(:)分割，
每個對之間用逗號(,)分割，
整個字典包括在花括弧({})

d = {key1 : value1, key2 : value2 }

鍵必須是唯一的，但值則不必。

值可以取任何資料類型，
但鍵必須是不可變的，如字串，數位或元組。
```
```
資料型態( Data Type)學習重點:
各種運算
各種內建函數
型態轉換
運算優先順序
```


# 字串(string)及其運算

# 列表(list)資料及其運算

# 字典(dict)資料及其運算 
