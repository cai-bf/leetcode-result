给定一个Excel表格中的列名称，返回其相应的列序号。

例如，

    A -> 1
    B -> 2
    C -> 3
    ...
    Z -> 26
    AA -> 27
    AB -> 28 
    ...
示例 1:

输入: "A"
输出: 1
示例 2:

输入: "AB"
输出: 28
示例 3:

输入: "ZY"
输出: 701  

```cpp
#include <cmath>
class Solution {
public:
    int titleToNumber(string s) {
        reverse(s.begin(), s.end());
        int len = s.length();
        int result = 0;
        for(int i=0; i < len; i++){
            result += (s[i]-'A'+1)*pow(26, i);
        }
        return result;
    }
};
```
