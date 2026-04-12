# Code 
```cpp
class Solution {
public:

    void change(int r, int c, int mr, int mc,
                vector<vector<int>>& image,
                int color, int temp) {
        if(mr < 0 || mc < 0 || mr >= r || mc >= c)
            return;
        if(image[mr][mc] != temp)
            return;
        image[mr][mc] = color;
        change(r, c, mr+1, mc, image, color, temp);
        change(r, c, mr-1, mc, image, color, temp);
        change(r, c, mr, mc+1, image, color, temp);
        change(r, c, mr, mc-1, image, color, temp);
    }

    vector<vector<int>> floodFill(vector<vector<int>>& image, int sr, int sc, int color) {
        
        int r = image.size();
        int c = image[0].size();
        
        int temp = image[sr][sc];
        if(temp == color)
            return image;
        change(r, c, sr, sc, image, color, temp);
        
        return image;    
    }
};
```
# ScreenShot
<img width="1766" height="855" alt="image" src="https://github.com/user-attachments/assets/d4e84ffa-805f-4bbc-bd2a-2d3ac1c86400" />
