```java
import java.util.*;
class Solution {
    public int solution(int[] citations) {
        Arrays.sort(citations);
        int len = citations.length;
        int max = citations[0]; 
        for(int i=0; i<len; i++){
            if(citations[i]> len-i){ 
                max=len-i;
                break;    
            }else if(citations[i]==len-i){
                max=citations[i];
                break;
            }else{
                max=citations[i];
            }
            
        }
        return max;
    }
}
```
