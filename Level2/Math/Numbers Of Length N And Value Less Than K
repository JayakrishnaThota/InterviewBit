public class Solution {
    public int solve(ArrayList<Integer> A, int B, int C) {
        String str=Integer.toString(C);
        int cl=str.length();
        int size=A.size();
        int d=size,d2;
        if(B>cl || C==0 || size==0)
            return 0;
        int zeros=A.lastIndexOf(0)-A.indexOf(0)+1;
        boolean zero=A.contains(0);
        int ans=0;
        if(B<cl){
            if(zero && B!=1)
                ans += size-1;
            else
                ans=size;
            for(int i=1;i<B;i++)
                ans *= size;
            return ans;
        }
        
        int dp[]=new int[B+1];
        int lower[]=new int[11];
        
        if(B==cl){
            
            for(int i = 0; i <= B; i++)
              dp[i] = 0;
            for(int i = 0; i <= 10; i++)
              lower[i] = 0;
            for(int i = 0; i < d; i++)
              lower[A.get(i) + 1] = 1;

            for(int i = 1; i <= 10; i++)
              lower[i] = lower[i-1] + lower[i]; 

                boolean flag = true;
                dp[0] = 0;
                for(int i = 1; i <= B; i++) {
                    int digit=str.charAt(i-1)-'0';
                  d2 = lower[digit];
                  dp[i] = dp[i-1] * d;
    
                  // For first index we can't use 0
                if(i == 1 &&  A.get(0) == 0 && B != 1)
                     d2 = d2 - 1;
    
                 //Whether (i-1) digit of generated number can be equal to (i - 1) digit of C.
                 if(flag)
                     dp[i] += d2;
             //Is digit[i - 1] present in A ?
                flag = flag & (lower[digit + 1] == lower[digit] + 1);
            }
            return dp[B];          
        
        }
        return 0;
        
    }
}
