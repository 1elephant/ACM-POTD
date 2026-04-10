# Code 
```cpp
class Solution {
public:
    string removeOuterParentheses(string s) {
        string res = "";
        int depth = 0;

        for (char c : s) {
            if (c == '(') {
                if (depth > 0) res += c;
                depth++;
            } else {
                depth--;
                if (depth > 0) res += c;
            }
        }

        return res;
    }
};
```
# ScreenShot
<img width="1918" height="872" alt="image" src="https://github.com/user-attachments/assets/29342149-5fef-4aac-85fd-d9ade683ca20" />
