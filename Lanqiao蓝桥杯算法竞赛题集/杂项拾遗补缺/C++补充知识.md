C++版本介绍
![[C++常见版本.png]]

```cpp
#include<bits/stdc++.h>//万能头文件
#include<string> // 使用string时的头文件 
//'\n'换行符比 endl 更快
typedef long long ll // 常用作为 long long 的定义缩写 

// cin cout 和 scanf printf 一般不混用

// 取消同步流方法
ios::sync_with_stdio(0), cin.tie(0), cout.(0);

// %s 遇到空格或回车即停下
scanf("%[^\n]", s); // [] 是一个正则表达式，表示只要不是回车就继续读入，解决s遇到空格就停止读入的问题

for(int i = 1; i <= n; i++) cout << a[i] << " \n"[i == n]; // " \n"[i == n]：字符串 " \n" 中索引为 i == n 的位置，取决于 i 是否等于 n。如果 i == n 为 true（即 i 是最后一个元素），则访问 " \n"[1]，即换行符 \n；如果 i != n，则访问 " \n"[0]，即空格 ' '。

cin >> s + 1; // 从 s[1] 开始输入
// cin 输入字符串也是遇到空格或回车就结束
for(int i = 1; s[i]; ++i) cout << s[i]; // s[i] 在不等于 '0' 时持续输出

string s;
getline(cin, s); // 这样可以将整行字符串（包含空格）输入进入s
string s1 = s.substr(0, 5); // 初始化string的方法：使用substr(开始位置，长度)
string s2(5, 'A'); // (个数，字符)

// std::string 类提供一个成员函数 c_str(), 用于返回一个指向以空字符结尾的C风格的字符串（即 const char* 类型， 由于printf 输出时需要将string转换为C风格的字符串进行输出）

char buf[100];
scanf("%s", buf);
string str(buf); // 用buf进行构造str
printf("str = %s\n", str.c_str()); // 输出str

string result = str1.append(",").append(str2);
string answer = str1 + "," + str2; // append 和 + 用于拼接字符串

str = "Hello World ！";
str.replace(7, 5, Universe); // 替换字符串，（字符串起始位置，长度）
cout << str ; // 输出为 Hello Universe ！
```







