
class Solution:
    def nthFibonacci(self, n: int) -> int:
        # Base cases
        if n == 0:
            return 0
        if n == 1:
            return 1
            
        # Initialize the first two terms
        prev2 = 0  # F(0)
        prev1 = 1  # F(1)
        
        # Calculate from 2 to n
        for i in range(2, n + 1):
            current = prev1 + prev2
            # Update previous terms for the next iteration
            prev2 = prev1
            prev1 = current
            
        return prev1

# Example Usage:
# n = 5
# sol = Solution()
# print(sol.nthFibonacci(n)) # Output: 5
