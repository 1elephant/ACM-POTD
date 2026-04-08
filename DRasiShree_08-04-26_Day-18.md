# Code
```cpp
class Solution {
public:
    string removeDuplicates(string s) {
        stack<char> s1;
        for(auto i:s){
            int y=0;
            if(!s1.empty()){
                char t=s1.top();
                if(t==i){
                    s1.pop();
                    y=1;
                }
            }
            if(y==0){
                s1.push(i);
            }
        }
        string ans = "";
        while(!s1.empty()){
            ans += s1.top();
            s1.pop();
        }
        reverse(ans.begin(), ans.end());

        return ans;    
    }
};
```
# Screenshot
<img width="1917" height="878" alt="image" src="https://github.com/user-attachments/assets/95dc330b-134d-4c2d-80ca-60430fca2012" />
