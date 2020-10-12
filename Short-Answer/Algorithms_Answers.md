#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
    # while loop -- n^3
        # a approaching n^3 via n^2
        # n^3/n^2 = n
        # The time complexity is O(n) because the runtime grows linearly with the input size.

b) 
    # for loop -- O(n)
        while loop -- (log(n))

The time complexity for the for loop is O(n). The time complexity for the while loop is O(log(n)) as the condition for the while loop is cut in half on every pass of the loop. Since they are nested you multiply them together for a resulting time complexity of O(n*log(n)).


c) In this recursive call the number of function calls is directly determined by the input size which makes it a linear time complexity O(n).

## Exercise II

Recursive Binary Search Strategy:

Find middle floor
mid = number of floors ( or high - low ) / 2

drop egg from mid, check if breaks,
if it breaks
    assume you need to go lower
    find new mid, setting the current mid - 1 as the new high, keeping the same low and run function again with new inputs
if it doesn't break
    check if you can go higher
    add 1 to floor and test if it breaks until you find that it does then end loop
if it doesn't break
    return floor

The algorithm involves cutting the condition in half with every pass of the loop until it finds a floor that doesn't break, which gives it O(log(n)). However, when it finds that floor it still has to check for a higher floor, adding 1 until it reaches the old midpoint as worst case, which would be another O(log(n)). The resulting time complexity would be (log(n) + log(n)) which simplifies to O(log(n)).