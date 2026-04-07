# Code - Basic
```cpp
class MyStack {
private:
    queue<int> q;
    
public:
    MyStack() {}
    
    void push(int x) {
        q.push(x);
        for (int i = 1; i < q.size(); i++) {
            q.push(q.front());
            q.pop();
        }
    }
    
    int pop() {
        int res = q.front();
        q.pop();
        return res;
    }
    
    int top() {
        return q.front();
    }
    
    bool empty() {
        return q.empty();
    }
};
```
 # ScreenShot
 <img width="1919" height="865" alt="image" src="https://github.com/user-attachments/assets/f04501d6-a85a-4ac2-81cd-89dcc5089ea0" />
