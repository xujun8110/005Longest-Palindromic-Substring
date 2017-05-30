# 005Longest-Palindromic-Substring
最长回文子串，回文就是字符串正着倒着读一样
Input: "babad"
Output: "bab"

暴击解法：n位字符串全部子字符串为o(n^2),每个字符串需要遍历一边o(n),因此时间复杂度o(n^3)

符合动态规划问题特征：
1.最优子结构       
  母问题的最优解包含其子问题的最优解，我们就称此问题具有最优子结构。即也就是说，子问题最优时，母问题通过优化一定能求得最优解 
2.子问题重叠       
  子问题本质上是和母问题一样的，只是问题的输入参数不一样，就可以称之为子问题重叠，这是动态规划解决问题的高效的本质所在，我们可以利用很多子问题具有相同的输入参数这一个性质，来减少计算量。 
3.问题存在边界       
  子问题在一定情况下就不存在子问题了， 我们称这种情况为问题存在边界，对于自顶向上和自底向下的方法，边界分别是问题的出口和入口。
4.子问题相互独立       
  个子问题在求解最优解时事相互独立的，即本自问题的求解和其他平行子问题是不相干的。当平行子问题解决后，选择权交给母问题时，它才会考虑各子问题之间的关系，是求最大值还是最小值，还是要做相关的运算得到母问题的最优解。
  
  符合第1 2类型的问题较多，即对于问题而言有最有子解法，能写出状态转移方程，回归到此问题，对于此题而言，符合回文的字符串子串也一定符合回文字符串，即包含子问题最优解，状态转移方程为dp[i][j] = (s.charAt(i) == s.charAt(j) && dp[i+1][j-1] = true)
  
public class Solution{
    public String longestPalindrome(String s) {
        int length = s.length();
        boolean dp[len][len]; 

        for(int i = 0; i < length; i++) {
            dp[i][i] = true;
        }

        for(int substringLen = 2; substringLen < len ; substringLen++) {
            for(int j = 0; j < length - substringLen; j++) {
                dp[]
            }
        }
    }
}
