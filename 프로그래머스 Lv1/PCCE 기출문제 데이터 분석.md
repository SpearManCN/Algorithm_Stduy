<image src="pictures/46.png" >

```java
import java.util.*;
class Solution {
    public int[][] solution(int[][] data, String ext, int val_ext, String sort_by) {
        int theVal = 0;
        int sortBy = 0;
        Map<Integer, Integer> tmp = new HashMap<>();
        if(ext.equals("code")){
            theVal = 0;
        }else if(ext.equals("date")){
            theVal = 1;
        }else if(ext.equals("maximum")){
            theVal = 2;
        }else if(ext.equals("remain")){
            theVal = 3;
        }
        if(sort_by.equals("code")){
            sortBy = 0;
        }else if(sort_by.equals("date")){
            sortBy = 1;
        }else if(sort_by.equals("maximum")){
            sortBy = 2;
        }else if(sort_by.equals("remain")){
            sortBy = 3;
        }
        List<Integer> tmp2 = new ArrayList<>();
        
        for(int i=0; i<data.length; i++){
            if(data[i][theVal]<val_ext){
                tmp.put(data[i][sortBy], i);
                tmp2.add(data[i][sortBy]);
            }
        }
        Integer[] tmp3 = tmp2.toArray(new Integer[tmp2.size()]);
        Arrays.sort(tmp3);
        int[][] result = new int[tmp.size()][4];
        for(int i=0; i<tmp.size();i++){
            result[i] = data[tmp.get(tmp3[i]) ];
        }
        return result;
    }
}
```
