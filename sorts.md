Bubble Sort-
 One thing to remember is that each sort can only be done once

 as it

 PASS 1
 38, 16, 27, 39, 12
16, 38, 27, 39, 12
16, 27, 38, 39, 12
16, 27, 38, 12, 39
16, 27, 12, 38, 39
16, 12, 27, 38, 39
12, 16, 27, 38, 39

Heres the code
def bubble_sort(a_list):
for i in range(len(a_list) - 1, 0, -1):
for j in range(i):
if a_list[j] > a_list[j + 1]:
temp = a_list[j]
a_list[j] = a_list[j + 1]
a_list[j + 1] = temp

Efficiency: O(n^2)


selection sort
----------------------------------------

Selection sort will locate the largest value in a list- and instantly put it at the end
and the second largest at the second last and so on.
EXAMPLE:
38, 16, 27, 39, 12
SCAN 1: 38, 16, 27, 12, 39
12, 16, 27, 38, 39

code for it:
def selection_sort(a_list):
for i, item in enumerate(a_list):
min_idx = len(a_list) - 1
for j in range(i, len(a_list)):
if a_list[j] < a_list[min_idx]:
min_idx = j
if min_idx != i:
a_list[min_idx], a_list[i] = \
a_list[i], a_list[min_idx]


Efficiency: O(n^2)


Insertation sort
-----------------------------

Insertion sort is kind of like bubble sort, only that instead of comparing the entire array over and over again, when it goes to sort an array, it compares all the numbers before it as well.

Let me explain:

say you have the list 
[2,3,1,12,3,14]

so it first looks at 2, 3 which are all sorted, then it moves on to 3, 1

switches those- BUT DOSENT MOVE ON
it then looks at 2 and 1 and switches those as well. So the numbers will get sorted no matter what.

Heres the code:
def insertion_sort(a_list):
for i in range(1, len(a_list)):
cur_val = a_list[i]
cur_pos = i
while cur_pos > 0 and a_list[cur_pos - 1] > cur_val:
a_list[cur_pos] = a_list[cur_pos - 1]
cur_pos = cur_pos - 1
a_list[cur_pos] = cur_val


Shell Sort
-----------------------------------
Shell sort is when you sort a whole array based on gaps and then reduce the gap

lemme explain:

array: [3,4,12,32,42,12,2,3,46]

if you took a gap of three, you would have
12,12,46- you sort these.

then sort the gap 2

4, 32, 12, 3

then gap 1- which is insertation sort.


