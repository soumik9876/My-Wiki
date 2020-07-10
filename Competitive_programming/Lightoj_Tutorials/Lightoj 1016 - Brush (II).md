Author: Soumik Roy

**<b>Hint:</b> In this problem, x axis doesn't matter since the brush can be moved along x axis and all dust points with same y axis can be cleaned with 
the same operation.

<b>Detailed tutorial:</b> If the brush is placed between y1 and y2 axis,then any dust point with y axis between y1 and y2 inclusive will be cleaned. Although there are 
2 axis in the input,x axis doesn't matter since the brush can be moved along x axis. And points with same y axis can also be treated as one.

<b>Sort and starting point:</b> After taking input,we sort all the y axis value in ascending order. A set can be used for this purpose since we don't need duplicate values. Then we take a starting/down point
of the brush. Initially the starting point can be the lowest y axis value.

<b>Iterate:</b> Then we iterate through the sorted y axis values. While iterating if the difference between current y axis value and starting value
becomes greater than the width of brush,then we change the starting point to current y axis value and increment our count by 1. 

We get our output after the iteration is completed. Complexity O(n).
