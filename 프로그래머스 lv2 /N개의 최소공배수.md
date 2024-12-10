```java
class Solution {
    public int solution(int[] arr) { 
        int tmp = arr[0]; 
        for(int i=1; i<arr.length ; i++){
            tmp = logic(arr[i],tmp);
        }
        return tmp;
    } 
    public int logic(int x, int y){
        int tmp = 0;
        if(x>y){
            tmp = x;
            x = y;
            y = tmp;
        }
        int max = 1;
        for(int i=1; i<=x; i++){
            if(x%i==0&&y%i==0){
                max = i;
            }
        }
        int result = x*y/max;
        return result;
    }
}
```
