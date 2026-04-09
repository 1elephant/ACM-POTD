# Code - Intermediate
```cpp
class Solution {
public:
    int evalRPN(vector<string>& tokens) {
        stack<int> nums;
        for (auto &i : tokens) {
            if (i == "+" || i == "-" || i == "*" || i == "/") {
                int x = nums.top(); nums.pop();
                int y = nums.top(); nums.pop();
                int z = 0;
                if (i == "+") z = y + x;
                else if (i == "-") z = y - x;
                else if (i == "*") z = y * x;
                else if (i == "/") z = y / x;
                nums.push(z);
            } else {
                nums.push(stoi(i)); // number
            }
        }
        return nums.top();
    }
};
```
# ScreenShot
<img width="1919" height="858" alt="image" src="https://github.com/user-attachments/assets/57824125-ee04-4f51-b89e-b72a8a9eac87" />

