# Search_a_2D_MATRIX
You are given an m x n integer matrix matrix with the following two properties:  Each row is sorted in non-decreasing order. The first integer of each row is greater than the last integer of the previous row. Given an integer target, return true if target is in matrix or false otherwise.


class Solution:
    def search_matrix(self, matrix:List[List[int]]) -> bool:
          
          # iterate though the list of list as outer loop then iterate through list of integers as inner loop
          for lst in matrix:
              for num in lst:
                  # matrix is on ascending order so when the current number is greater than target we can return False and skip the rest of the matrix
                  # return True if current number is equal to the target, else continue forward
                  if num == target:
                      return True
                  elif num < target:
                      continue 
                  elif num > target:
                      return False
    
