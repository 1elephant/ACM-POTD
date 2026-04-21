# Code 
```cpp
long per(int n,int r){
    long p=1;
    if(r>n)return 0;
    for(int i=1;i<=r;i++){
        p=p*(n-r+i)/i;
    }


    return p;
}
int climbStairs(int n) {
    int ways=0;
    if(n==0){
        return 0;
    }
    else{
        for(int i=0;i<=n;i++){
            if((n-i)%2==0){
                ways=ways+per((n+i)/2,i);
            }
        }
        return ways;   

    }
 
}
```
# ScreenShot
<img width="1919" height="823" alt="image" src="https://github.com/user-attachments/assets/d056cbd4-1254-489d-9ff4-79dd5cb9a7dc" />
