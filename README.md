# DSA-lab5Lab 5: LeetCode Problem and Vectors
Objective
In this lab, we are working on a LeetCode problem involving vectors, where we will implement a solution using C++ (or your preferred language). The goal is to practice using vectors for efficient data manipulation and solving algorithmic problems.

Problem Statement
Provide the description of the LeetCode problem you're working on. For example:

Problem: LeetCode Problem #XXX: Problem Name

You can provide a brief description of the problem here.
Example Problem:

Problem: Given an array of integers, find the maximum product of two integers in the array. Return the product of the two integers that give the highest product.
Input:
A vector of integers (e.g., nums = [2, 3, -2, 4]).
Output:
An integer representing the maximum product of two integers.
Approach
Step 1: Analyze the Problem
Begin by understanding the problem statement and identifying any edge cases (e.g., empty vectors, one element, etc.).
Step 2: Define the Solution
Using vectors in C++ (or your preferred language), we will iterate over the input array and use a specific algorithm to find the solution.
In this case, you might want to use a brute-force solution or an optimized approach (e.g., sorting, dynamic programming, etc.).
Step 3: Write the Code
Write the code that implements the solution. Here's an example in C++:
cpp
Copy code
#include <vector>
#include <algorithm>
using namespace std;

int maxProduct(vector<int>& nums) {
    if (nums.size() == 0) return 0;
    int max_product = nums[0];
    int min_product = nums[0];
    int result = nums[0];

    for (int i = 1; i < nums.size(); i++) {
        if (nums[i] < 0) swap(max_product, min_product);
        max_product = max(nums[i], max_product * nums[i]);
        min_product = min(nums[i], min_product * nums[i]);
        result = max(result, max_product);
    }
    
    return result;
}
Step 4: Test the Code
Test the code using sample test cases, and ensure the solution works for both small and large input sizes.
Vector Explanation
A vector is a dynamic array that can resize itself automatically when elements are added or removed. It's part of the C++ Standard Library.
The operations commonly used with vectors include:
push_back(): Adds an element to the end of the vector.
pop_back(): Removes the last element.
size(): Returns the number of elements in the vector.
[index]: Access elements by index.
Example:
cpp
Copy code
vector<int> nums = {2, 3, -2, 4};
int result = maxProduct(nums);
Results
Provide the expected output or results of running the code on sample test cases.
Example Test Case 1:

Input: [2, 3, -2, 4]
Output: 6 (Maximum product is 2 * 3 = 6)
Example Test Case 2:

Input: [-2, 0, -1]
Output: 0 (Maximum product is 0)
Conclusion
In this lab, we solved the LeetCode problem using vectors and applied algorithms to find the optimal solution efficiently. The use of vectors allowed us to manipulate data easily and solve the problem within the constraints provided.
