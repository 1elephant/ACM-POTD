# Code- Intermediate
```cpp
class MinStack {
public:
    stack<int> s;
    stack<int>mins;
    MinStack() {
        
    }
    
    void push(int val) {
        s.push(val);
        if(mins.empty()){
            mins.push(val);
        }
        else{
            int t=mins.top();
            mins.push(min(t,val));
        }
        
    }
    
    void pop() {
        mins.pop();
        s.pop();
        
    }
    
    int top() {
        int t=s.top();
        return t;    
    }
    
    int getMin() {
        int t=mins.top();
        return t;
        
    }
};
```
# ScreenShot
<img width="1910" height="812" alt="Screenshot 2026-04-05 071032" src="https://github.com/user-attachments/assets/17f9305c-db8a-44b7-9a08-99e4ece6c95b" />


