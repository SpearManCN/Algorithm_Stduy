<image src="pictures/41.png" >

```java
class Solution {
    public int solution(int[] bandage, int health, int[][] attacks) {
        int maxHeal = health;
        int gapTime = 0;
        int maxTime = bandage[0];
        int perHeal = bandage[1];
        int successHeal = bandage[2];
        int pastTime = 0;
        for(int i=0; i<attacks.length; i++){
            gapTime=attacks[i][0]-pastTime;
            pastTime = attacks[i][0];
            health+=(gapTime-1)*perHeal+((gapTime-1)/maxTime)*successHeal;
            if(health>=maxHeal){
                health = maxHeal;
            }
            health=health-attacks[i][1];
            if(health<=0){
                return -1;
            }
        }
        return health;
    }
}
```
