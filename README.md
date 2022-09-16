# Methods-in-leetcode

sum也挺费时的。用一次就好，不要用sum loop。

例如这题：问一个数的左右之和是否一致。方法一用了sum一次；
第二个方法用sum在loop，所以很慢。

    def balancedSums(arr):
      # Write your code here
      left = 0
      right = sum(arr)
      for c in arr:
          left+=c
          # left become a dynamic addition
          if left - c == right - left:
              return "YES"
      return "NO"

      # also right, but exceed the time limit
      # if len(arr) ==1:
      #     return "YES"

      # for i in range(1,len(arr)-1):
      #     if sum(arr[:i]) == sum(arr[i+1:]):
      #         return "YES"
      # return "NO"
