# Code - Intermediate
```cpp
class Solution {
public:
    ListNode* removeNthFromEnd(ListNode* head, int n) {
        ListNode* dummy=new ListNode(-1,head);
        ListNode* l=dummy;
        ListNode* r=dummy;
        for(int i=0;i<n;i++){
            r=r->next;
        }
        while(r->next!=NULL){
            r=r->next;
            l=l->next;
        }
        if(l==dummy){
            return head->next;    
        }
        else if(l->next->next!=NULL){
            l->next=l->next->next;
        }
        else{
            l->next=NULL;
        }
        return head;    
    }
};
```
# ScreenShot
<img width="1893" height="871" alt="Screenshot 2026-03-29 081536" src="https://github.com/user-attachments/assets/3574ca37-3642-42f7-ae77-9ef4b2c88ba5" />
