```java
class Solution {
    public String solution(String s) {
         
        s = s.toLowerCase(); 
        int length = s.length();  
        String[] tmp = s.split("");  

        boolean flag = true; 
        for(int i=0; i<length; i++){ 
            if(tmp[i].equals(" ")){
                flag=true;continue;
            }
            if(flag){
                tmp[i]=tmp[i].toUpperCase();
                flag=false;
            }
            
        }
        return String.join("",tmp);
        
        
        
    }
}
```
