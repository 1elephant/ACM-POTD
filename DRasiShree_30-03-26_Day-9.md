# Code - Intermediate
```cpp
class Solution {
public:
    ListNode *detectCycle(ListNode *head) {
        ListNode* l=head;
        ListNode* r=head;
        while(r!=NULL && r->next!=NULL){
            r=r->next->next;
            l=l->next;
            if(r==l){
                l=head;
                while(r!=NULL){
                    if(l==r){
                        return r;
                    }
                    l=l->next;
                    r=r->next;
                }
            }
        }
        return NULL;    
    }
};
```

# ScreenShot
<img width="1902" height="813" alt="Screenshot 2026-03-30 154757" src="https://github.com/user-attachments/assets/b9a8d91e-445e-4920-90f7-8d2c4ff2228b" />

