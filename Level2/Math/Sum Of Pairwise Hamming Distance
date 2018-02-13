public class Solution {
    // DO NOT MODIFY THE LIST. IT IS READ ONLY
    public int hammingDistance(final List<Integer> A) {
        int n = A.size();
        int dist = 0;
        for(int i = 0; i < 31; i++) {
            int oneCount = 0;
            for(int j = 0; j < n; j++) {
                int num = A.get(j);
                oneCount += (num & 1 << i) != 0? 1 : 0;
            }
            int zeroCount = n - oneCount;
            dist += (2L * oneCount * zeroCount) % 1000000007;
            dist = dist % 1000000007;
        }
        return dist;
    }
}
