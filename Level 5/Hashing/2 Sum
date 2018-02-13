public class Solution {
    // DO NOT MODIFY THE LIST. IT IS READ ONLY
    public ArrayList<Integer> twoSum(final List<Integer> A, int B) {
        ArrayList<Integer> result = new ArrayList();
        Map<Integer, Integer> map = new HashMap();
        for(int i=0;i<A.size();i++){
            int a = A.get(i);
            if(map.containsKey(B-a)){
                result.add(map.get(B-a));
                result.add(i+1);
                return result;
            }
            if(!map.containsKey(a))
            map.put(a, i+1);
        }
        return result;
    }
}
