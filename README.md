# CSCI313-HomeWorkOne-
White Pages for Homework One
*** Question 1 ***

*** Question 2 ***
I was not able to implement the linked binary search, however I did implement the iterative and recursive binary searches.
	Code provided by the professor was used for the iterative and recursive binary searches. 
vector<int> was used to create arrays of size 1 and 10 million, vectors were used to be able to use the generate and sort functions which will be described later. Next, the generate function was used to fill the array. Generate is a pre-existing template in c++. It takes in a beginning, ending, and random variable. Sort, another pre- existing template, was used to sort the array. 
	I began with the array of size 1 million. The chrono library was used to time the searches. timerStart and timerStop set to high_resolution_clock::now(), which is the most precise clock in the chrono library. timerStart and timerStop are put around binarysearch, which is the recursive search, to be able to capture how long the search took. binarySearch took in the parameters of array, the array of size 1 million, started from the first int 0, went to the last int 1000000 - 1, and had a target of also 1000000 - 1 so it would run through the entire array. Then, duration finds out how long the search took to run by subtracting timerStop from timerStart. Finally to show how long the search took I cout duration.count which stores the time it took the search to run.
	These steps are then repeated for the iterative binary Search and the whole process is repeated for the array of 10 million ints

*** Question 3 ***
For question 3 I had to sort a 2D array by doing various methods of sorting. The purpose of selection sort constantly finding the minimum element and is assigning it as the minimum value. If we think about it, it breaks it up into two parts a sorted one and an unsorted. It searches the whole list and finds the smallest value placing it as the first position of the sorted part. Then it continues at the second position and looks for the min value to place in the sorted part again. It keeps doing this to the rest of the array, eventually placing them in order. For the selection sorting aspect of this question what I did was implement 4 for loops. One of them goes through each row, the other one through each column, and finally the last two are inner loops that go through each position in each row or column. The first inner loop starts off by sorting the first row, it initializes the min row and col value at 0 as well as the whole matrix at 0,0. Then moving through the positions of that column it keeps changing that min value If there exists a smaller number. After it sorts through the rest of the rows proceeding to sort the columns as well once it’s done it moves on to the row on and so forth. At the end of this we get the min value and it is put at the front till it is sorted. This process isn’t very time efficient, it takes a longer time especially since we have a function containing 4 for loops. Next, we have bubble sorting, which is a sorting algorithm that compares elements and swaps if they’re not in order. I implemented 3 for loops one goes through the rows, the second one goes through the columns and the 3rd one is used to compare the current value to the one before it. I added an if statement that checks the two values and swaps them if the second one is smaller than the first. This process is repeated through every row in the matrix, sorting the values from min to max but only in that row. Now because I am missing another for loop so that it also sorts by columns, I kept trying to implement it but I kept getting lost and confused so it wasn’t working out which is why this only sorts my program by rows. These were my two separate functions for sorting, in my main function I simply declared a 3x3 matrix with numbers to order. I also initialized the total number of rows and columns so that they can be used in the bubble and selection sort functions. In addition, I made a simple print function that just displays the matrix in its 3x3 form. 
*** Question 4 ***
    For Question 4, there are four major parts of the program, the node class, the linked list class, the function for the arrays, and main. The class node contains int info, this will be the part of the node that will contain the data. Node* link is the link that connects the nodes to each other. This node class is fundamental to creating the nodes for our linked list and the linked list class 
	  The linked List is the most complex class of this program and the one that took the most time to create. This class contains two private elements, Node* head and Node* tail. They are both private to make sure that the user cannot mess around with these two elements. The head will be the start of the linked list, while the tail will be the end of the linked list. The class contains one default constructor. This default constructor initiates the head and tail to NULL to make sure they don’t point to anywhere they do not need to. The function addNode takes in element int x and adds it to the linked list. The addNode function creates a node called temp, temp will be a node that gets added to the linked list. The if statement (head == null) checks if there is nothing in the linked list, if nothing is there, the head and tail will become temp, temp becomes the first and last node. If there is something in the linked list, the else statement will make sure to make the tail point to the temp, making the temp the last node of the linked list. 
	  The printingList function takes in a Node print and will print out the contents of that node. A Node* temp will be created; node temp will point to node print. The while loop will run through the linkedList, only ending once it reaches the end, which is nullptr. Inside the while loop, the content of temp will be printed. Every single time the info of the node is printed, temp will be linked to the next node in the linked list. Function Node* getHead will return the head of the linkedList.
	  Function swapLinkedList takes two nodes swaps the info of two nodes of the linked list. Temp will hold the info of nodeOne and nodeOne will get the info of nodeTwo. NodeTwo will get the info of temp.
	Function bubbleSortLinkedList takes Node* head and will sort the linked list through bubble sort. Int swapped is the check for the while loop, will change from 0 to 1 depending on the conditions of the loops. There are two node, leftPtr and rightPtr , the leftPtr will point to the start and rightPtr will start at the end. Inside the do loop, there is a while loop that will go through the linked list. There is an info statement that will check if info of the left is greater than info of the right, if this is true the leftPtr will switch with node to the next. Int swapped will change be changed to 1, allowing for the while loop continue. if the statement is false, the other elements will be checked. 
*** Question 5 ***
	  Functions sortedInsert and insertionSortLinkedList are two functions that will sort the linked list through insertion sort. sortedInsert will help with sorting by returning the head after insertion. insertionSort will sort the linked list through insertion sort. 
	  Next up are function prototypes, that will help throughout main. In the main, I created an array of 10 and filled it with random numbers between 1 – 10. The array will be sorted by the bubble sort and insertion sort function. Using the LinkedList class, a linked link will be created. Elements of the array will be added to linked list. The linked list will be sorted by the bubble sort and insertion sort functions from the linked list class. timingSort at the end of the function will give the time of the function. 
	  The bubble sort function for the array uses two for loops to go through the array once and to swap the elements. The first for loop will go through the array, while the second will check the elements in the position, will swap the elements, with the use of the swap function that I create. If the conditions of the if statement are met, elements will be swapped. 
	  The insertion sort function for the array has one for loop and one while loop. The for loop will go through the array, while the while loop is in charged with insertion the elements to the current positions. 
Selection and insertion sort are used as comparable sorts because they both have a best and worst case performance of n^2. Selection sort and Insertion code is the same as provided by the professor. trueSort function is created as a multi level sort. The function uses insertion sort if the size of the array is less than ten and selection sort if it is greater than ten. 
	In the main function, srand(time(nullptr)) is used to randomize the values in the array. Int n is randomized by mod 30 +1 so the size of the array will be between 1 to 30. N is then placed inside the array. Next, a for loop is run from 0 to n to input a random number for each index. The numbers are then sorted by the trueSort function, which decides which sort is used based on the size of the array, from low to high. Finally, another for loop is used from 0 to n to display the sorted ints.

*** Question 6 ***
*** Question 7 ***
*** Question 8 ***
*** Question 9 ***
*** Question 10 ***
*** Question 11 ***
	A base class of Restaurant is created with a pure virtual function menu and a vector<string> vectorMenu(), which will hold the data for the menu of the restaurant. Then, classes for and italian, greek, and chinese restaurants were made. All three restaurants inherit the Restaurant class. Vector<string> menu() has to be overloaded because it is a pure virtual function, if not it will cause errors. Vector<string> menu() is overloaded in all the restaurant classes and use vectorMenu that they inherited and use .push_back to return their menus. Next, every restaurant class also has a for loop which inherits vectorMenu and will return the menu.
	readerRobot is a templated class that takes in any restaurant and prints out the menu. readerRobot prints the menu by taking in a restaurant class and creating a reader. Then you can use the reader.printMenu(nameoftherestaurant) to print the menu. Finally, in the main function the names of the restaurants are declared and the readerRobot template is used to print out the menu.

*** Question 12 ***
*** Question 13 ***
