# Code -Intermediate
```cpp
class Solution {
public:
    ListNode* swapPairs(ListNode* head) {
        if(head==NULL || head->next==NULL) return head;

        ListNode* l=head;
        ListNode* r=head->next;
        ListNode* prev=NULL;
        int y=0;

        while(l!=NULL && r!=NULL){
            ListNode* temp=r->next;
            r->next=l;
            l->next=temp;
            if(y==0){
                head=r;
                y=1;
            }
            if(prev!=NULL){
                prev->next=r;
            }
            prev=l;
            if(temp==NULL || temp->next==NULL) break;
            l=temp;
            r=temp->next;
        }

        return head;
    }
};
```
# ScreenShot
<img width="1903" height="802" alt="image" src="https://github.com/user-attachments/assets/6729aa34-951a-45d4-ab55-2a36611c2fba" />
