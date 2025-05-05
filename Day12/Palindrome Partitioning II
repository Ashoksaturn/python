class Solution(object):
    def minCut(self, s):
        pal_memo = {}
        cut_memo = {}

        def isPalindrome(i, j):
            if i >= j:
                return True
            if (i, j) in pal_memo:
                return pal_memo[(i, j)]
            if s[i] != s[j]:
                pal_memo[(i, j)] = False
                return False
            pal_memo[(i, j)] = isPalindrome(i + 1, j - 1)
            return pal_memo[(i, j)]

        def helper(i):
            if i == len(s):
                return 0
            if i in cut_memo:
                return cut_memo[i]

            min_cuts = float('inf')
            for j in range(i, len(s)):
                if isPalindrome(i, j):
                    min_cuts = min(min_cuts, 1 + helper(j + 1))

            cut_memo[i] = min_cuts
            return min_cuts

        return helper(0) - 1
