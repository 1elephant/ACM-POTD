#Code-Intermediate
```cpp
class Solution {
public:
    void sortColors(vector<int>& nums) {
        vector<int> hash(4,0);
        for(auto n:nums){
            hash[n]++;
        }
        int n=0;
        for(int i=0;i<4;i++){
            for(int j=0;j<hash[i];j++){
                nums[n]=i;
                n++;
            }
        }    
    }
};
```

#Screenshot

<img width="1917" height="884" alt="image" src="https://github.com/user-attachments/assets/2417f09e-6247-4279-b702-7f3de20d93c1" />
