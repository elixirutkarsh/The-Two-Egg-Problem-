# The-Two-Egg-Problem
You are given two identical eggs and a 100-story building. The goal is to find the highest floor from which an egg can be dropped without breaking. You need to determine the minimum number of attempts required to find the solution, using the fewest number of egg drops possible.
Solution:
To solve this problem optimally, you can use a technique called binary search. Here's how:

Start by dropping the first egg from the 50th floor.
If the egg breaks, you know it will break from any floor above, so you can now use the second egg to perform a linear search from the 1st floor up to the 49th floor, one floor at a time, until it breaks. The total number of drops will be at most 50 in this case.
If the first egg doesn't break when dropped from the 50th floor, you know it will not break from any floor below. Move to the 75th floor and repeat the process. If the egg breaks, perform a linear search from the 51st floor up to the 74th floor using the second egg. If the egg doesn't break, move to the 88th floor, and so on, dividing the remaining floors in half each time.
By using this binary search approach, you can find the highest floor in a maximum of 7 drops in the worst-case scenario.
