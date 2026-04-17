# Code 
```cpp
class Solution {
public:
    int diameterOfBinaryTree(TreeNode* root) {
        int ans=0;
        function<int(TreeNode*)> h=[&](TreeNode* node)->int{
            if(!node)return 0;
            int l=h(node->left),r=h(node->right);
            ans=max(ans,l+r); return 1+max(l,r);
        };
        h(root); return ans;
    }
};
```
# ScreenShot
<img width="1919" height="781" alt="image" src="https://github.com/user-attachments/assets/fd67d7e7-95d6-480c-b37a-e8084839e38c" />
