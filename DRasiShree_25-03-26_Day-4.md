#Code-Intermediate
```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& numbers, int target) {
        int len=numbers.size();
        int l=0;
        int r=len-1;
        while(l<r){
            if(numbers[l]+numbers[r] ==target){
                return {l+1,r+1};
            }
            else if(numbers[l] +numbers[r]>target){
                r--;
            }
            else{
                l++;
            }
        }
        return {};    
    }
};
```
#ScreenShot

<img width="1917" height="875" alt="Screenshot 2026-03-25 072151" src="https://github.com/user-attachments/assets/6822f54a-6eb1-4ebf-b37c-0dd878347e46" />
