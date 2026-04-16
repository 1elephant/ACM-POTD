# Code
```cpp
class Solution {
public:
    void fun(TreeNode* node){
        if(node==NULL) return;
        if(node->left!=NULL || node->right!=NULL){
            swap(node->left,node->right);
        }
        fun(node->left);
        fun(node->right);
    }
    TreeNode* invertTree(TreeNode* root) {
        TreeNode* temp=root;
        fun(temp);
        return root;
        
    }
};
```
# Screenshot

