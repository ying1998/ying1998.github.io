#c++ Learning

##<<左移运算符


```c++
if (access(CRL_SERIAL_NUMBER, F_OK) == -1) {
            std::fstream fs;
            fs.open(CRL_SERIAL_NUMBER, std::fstream::out);
            if (!fs) {
                printf("Init: create file: %s Failed!\n", CRL_SERIAL_NUMBER);
                return COMMON_ERROR;
            }
            fs<<0;
            fs.close();
        }
```
运算符重载，就是对已有的运算符重新进行定义，赋予其另一种功能，以适应不同的数据类型
```fs<<0;```
中```<<```就是运算符重载。把0写入到fs中。

在 C++ 中，左移运算符```<<```可以和 ```cout``` 一起用于输出，因此也常被称为“流插入运算符”或者“输出运算符”。实际上，```<<```本来没有这样的功能，之所以能和 ```cout`` 一起使用，是因为被重载了。

```c++
std::fstream fs;
```
fstream 继承自iostream --> 要包含头文件```#include<fstream>```

```c++
file2<<"I Love You";
```
向文件写入字符串"I Love You"

```c++
int i;
file1>>i;
```
从文件输入一个整数值。

另外：在c++中是什么意思m=s[0]<<1;?

<<是左移位运算符，比如s[0]和m均是char类型的数据等于179，写成二进制数就是10110011，这时s[0]<<1，即计算左移一位(二进制的1位)，该数值变为01100110，最高位被移出了左边(被舍弃)，右边补0，这个左移相当于对s[0]乘以2。结果会被赋值给m。

##
