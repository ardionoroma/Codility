# Codility
Solution from some Codility lessons

This repository contains solution from some lessons in Codility. I wrote variables name mostly in Bahasa Indonesia. Try your best first before looking at my solution.

1. Binary Gap\n
This lesson's goal is to determine the longest binary gap in a binary number. For example, 2113 has a binary number 100001000001. There are two binary gaps there, the first one is the 4 of 0s, and the second one is 5 of 0s. Return the longest binary gap. In this example (2113), the function should return 5.\n
The logic/algorithm of this program is:\n
o Create an array to collect the binary gap possibilities from that number, also variables to detect the head and tail index of the binary gap.\n
o Change the integer number to a binary string.\n
o From the first until the last character from that binary string, check, if it is '1', then set the head index, if '1' is found again, set its index as the tail.\n
o Insert the difference between tail and head to the collector array. Don't forget to substract it with one because we work with array.\n
o Set the last tail index as head index, find another '1' again, set it as tail index again and so on.\n
o Return the largest number in the collector array.\n

2. Cyclic Rotation\n
This lesson's goal is to create right shifted A array in N shifts. The last element will be shifted as the first element. For example we have an array A{3,8,9,7,6}. If we shifted it to the right once it will result A{6,3,8,9,7}. So if the function is function(A{3,8,9,7,6}, 3) it will shift the array three times to the right as A{9,7,6,3,8}. Return the shifted array.\n

I create two functions to make it easier. First is the function for shifting the array to the right, let's called it shifting(). The second is a main function for shifting the array N times and updating the array elements' position, let's called it solution().\n
The logic/algorithm of this program is:\n
o For the shifting(), I started from the last element, and decrementing one by one to the left. So the main idea of this function is to drag the last element, changing its position one by one to the first position, and return the shifted array.\n
o For the solution(), I just updated the array's arrangement N times, then return the array as a solution.\n
