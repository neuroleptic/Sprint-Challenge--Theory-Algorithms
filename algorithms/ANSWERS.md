## Exercise 1

a) O(n)

b) O(log(n))

c) O(sqaure_root(n))

d) O(n * log(n))

e) O(n^3)

f) O(n)

g) O(n)


## Exercise 2

a) 
```
function linearMaxDifference(nums) {
  let maxDiff = 0;
  let smallestElement = nums[0];
  let temp;
  for(let i = 1; i < nums.length; i++) {
    temp = nums[i] - smallestElement;
    if(temp > maxDiff){
    	maxDiff = temp;
    }
    if(nums[i] < smallestElement) {
    	smallestElement = nums[i];
    }
  }
  return maxDiff;
}
```

b) Each round consists of dropping an egg off of the middle of the remaining floors (floor n / 2 for the first round). If the egg breaks, only consider floors below the middle floor in future rounds. If the egg does not break, only consider floors above the middle floor in future rounds. Continue until there is only 1 remaining floor. Each round reduces the number of floors to check by half, so the run time will be O(log(n)).

## Exercise 3

a) It will be O(n^2). Each partition will result in an array of size 1 and an array of size 1 less than the previous level in the recursion tree. Therefore, the recursion tree will have n levels. The run time of the work performed at each level of the recursion tree is O(n). Therefore, the run time will be O(n * n).

b) It will be O(n * log(n)). Each partition reduces the size of the array to sort by half, so there will be log(n) levels in the recursion tree. The run time of the work performed at each level of the recursion tree is O(n). Therefore, the run time will be O(n * log(n)).