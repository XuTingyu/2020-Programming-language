# 
```
#include <iostream>
using namespace std;
 
// 函式宣告
int max(int num1, int num2);
 
int main ()
{
   // 區域變數聲明
   int a = 100;
   int b = 200;
   int ret;
 
   // 調用函數來獲取最大值
   ret = max(a, b);
 
   cout << "Max value is : " << ret << endl;
 
   return 0;
}
 
// 函數返回兩個數中較大的那個數
int max(int num1, int num2) 
{
   // 區域變數聲明
   int result;
 
   if (num1 > num2)
      result = num1;
   else
      result = num2;
 
   return result; 
}
```

## 
```
#include <iostream>
using namespace std;
 
int sum(int a, int b=20)
{
  int result;
 
  result = a + b;
  
  return (result);
}
 
int main ()
{
   // 區域變數聲明
   int a = 100;
   int b = 200;
   int result;
 
   // 調用函數來添加值
   result = sum(a, b);
   cout << "Total value is :" << result << endl;
 
   // 再次調用函數
   result = sum(a);
   cout << "Total value is :" << result << endl;
 
   return 0;
}

```
