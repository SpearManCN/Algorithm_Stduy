<image src="pictures/31.png" >

```java
class Solution {
    public int solution(String[][] board, int h, int w) {
        String color = board[h][w];
        int count = 0;
        if(board.length>h+1){ //밑
            if(board[h+1].length>w){
                if(board[h+1][w].equals(color)){
                    count++;
                }
            }
        }
        if(h>0&&board[h-1].length>w){ //위
            if(board[h-1][w].equals(color)){
                count++;
            }
        }
        if(board[h].length>w+1){ //오
            if(board[h][w+1].equals(color)){
                count++;
            }
        }
        
        
        if(w>=1&&board[h][w-1].equals(color)){ //왼
            count++;
        }
        return count;
    }
}

```
