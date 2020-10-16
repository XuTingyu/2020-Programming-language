# python決策與選擇結構
```
[1]if
[2]if ...elsif
[3]if ...else
[4]if ...elsif ...else
[5]各種判斷條件
   AND
   OR
```
```
單向判斷式（if⋯）: 是非題｜對的才要做
雙向判斷式（if⋯else）: 二選一｜一定要選的
多向判斷式（if⋯elif⋯else）: 多選一｜一定要選的
```
```
程式流程控制　之 選擇(判斷) SELECTION /DECISION
Python 程式碼縮排
Python 語言以冒號「:」及縮排來表示程式區塊
縮排為 1 個 Tab 鍵或 4 個空白鍵
PS: Python沒有switch

https://www.w3schools.com/python/python_conditions.asp
```
# [1]if
```
a = 33
b = 200

if b > a:
  print("b is greater than a")
```
```
a = 33
b = 20

if b > a:
  print("b is greater than a")
```
# [2]if ...elsif
```
a = 32
b = 33

if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")

```
```
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```
```
a = 35
b = 33

if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```

# 雙向判斷式（if⋯else）: 二選一｜一定要選的
```
a = 200
b = 33

if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```
# [4]if ...elsif ...else  多選一｜一定要選的
```
a = 200
b = 33

if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```
# [5]各種判斷條件   AND  OR
```
#判斷是否為閏年
```
```
year= eval(input("請輸入年"))

if ((year%400==0) or (year%4==0 and year%100!=0)):
  print("{0} 是閏年".format(year))
else:
  print("{0} 不是閏年".format(year))
```
# 歲月匆匆程式開發
```
輸入:年月日
輸出:已經過了多少日
```
```
import time

date = time.localtime()	
print(date)
```
```
year, month, day = eval(input("請輸入年月日"))
year, month, day

請輸入年月日2019,5,22
(2019, 5, 22)
```
```
import time


#date = time.localtime()		#取得目前的日期時間
#year = date[0]
#month = date[1]
#day = date[2]

year, month, day = eval(input("請輸入年月日::"))
```
```
day_month = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]

if year%400==0 or (year%4==0 and year%100!=0):	
  day_month[1] = 29
```
```
if month==1:
    print(day)
else:
    print(sum(day_month[:month-1])+day)
```
# 多向判斷式（if⋯elif⋯else）:收銀台程式開發
```
百貨公司週年慶活動血拼大打折，
吸引很多顧客上門，
公司決定再加碼回饋客戶，

只要客戶消費
金額在 100000 元以上就打八折，
金額在 50000 元以上就打八五折，
金額在 30000 元以上就打九折，
金額在 10000 元以上就打九五折，
金額在 10000 元以下就不打折

請幫該公司設計這個收銀台的程式，
輸入顧客購買金額後，計算顧客應付的金錢。
```
```
money = int(input("請輸入購物金額："))

if(money >= 10000):
    if(money >= 100000):
        print(money * 0.8, end=" 元\n")  #八折
    elif(money >= 50000):
        print(money * 0.85, end=" 元\n")  #八五折
    elif(money >= 30000):
        print(money * 0.9, end=" 元\n")  #九折
    else:
        print(money * 0.95, end=" 元\n")  #九五折
else:
    print(money, end=" 元\n")  #未打折
```
