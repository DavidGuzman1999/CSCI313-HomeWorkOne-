# CSCI313-HomeWorkOne-
White Pages for Homework One
*** Question 1 ***
*** Question 2 ***
*** Question 3 ***

*** Question 4 ***
    For Question 4, there are four major parts of the program, the node class, the linked list class, the function for the arrays, and main. The class node contains int info, this will be the part of the node that will contain the data. Node* link is the link that connects the nodes to each other. This node class is fundamental to creating the nodes for our linked list and the linked list class 
	  The linked List is the most complex class of this program and the one that took the most time to create. This class contains two private elements, Node* head and Node* tail. They are both private to make sure that the user cannot mess around with these two elements. The head will be the start of the linked list, while the tail will be the end of the linked list. The class contains one default constructor. This default constructor initiates the head and tail to NULL to make sure they don’t point to anywhere they do not need to. The function addNode takes in element int x and adds it to the linked list. The addNode function creates a node called temp, temp will be a node that gets added to the linked list. The if statement (head == null) checks if there is nothing in the linked list, if nothing is there, the head and tail will become temp, temp becomes the first and last node. If there is something in the linked list, the else statement will make sure to make the tail point to the temp, making the temp the last node of the linked list. 
	  The printingList function takes in a Node print and will print out the contents of that node. A Node* temp will be created; node temp will point to node print. The while loop will run through the linkedList, only ending once it reaches the end, which is nullptr. Inside the while loop, the content of temp will be printed. Every single time the info of the node is printed, temp will be linked to the next node in the linked list. Function Node* getHead will return the head of the linkedList.
	  Function swapLinkedList takes two nodes swaps the info of two nodes of the linked list. Temp will hold the info of nodeOne and nodeOne will get the info of nodeTwo. NodeTwo will get the info of temp.
	Function bubbleSortLinkedList takes Node* head and will sort the linked list through bubble sort. Int swapped is the check for the while loop, will change from 0 to 1 depending on the conditions of the loops. There are two node, leftPtr and rightPtr , the leftPtr will point to the start and rightPtr will start at the end. Inside the do loop, there is a while loop that will go through the linked list. There is an info statement that will check if info of the left is greater than info of the right, if this is true the leftPtr will switch with node to the next. Int swapped will change be changed to 1, allowing for the while loop continue. if the statement is false, the other elements will be checked. 
	  Functions sortedInsert and insertionSortLinkedList are two functions that will sort the linked list through insertion sort. sortedInsert will help with sorting by returning the head after insertion. insertionSort will sort the linked list through insertion sort. 
	  Next up are function prototypes, that will help throughout main. In the main, I created an array of 10 and filled it with random numbers between 1 – 10. The array will be sorted by the bubble sort and insertion sort function. Using the LinkedList class, a linked link will be created. Elements of the array will be added to linked list. The linked list will be sorted by the bubble sort and insertion sort functions from the linked list class. timingSort at the end of the function will give the time of the function. 
	  The bubble sort function for the array uses two for loops to go through the array once and to swap the elements. The first for loop will go through the array, while the second will check the elements in the position, will swap the elements, with the use of the swap function that I create. If the conditions of the if statement are met, elements will be swapped. 
	  The insertion sort function for the array has one for loop and one while loop. The for loop will go through the array, while the while loop is in charged with insertion the elements to the current positions. 

*** Question 6 ***
*** Question 7 ***
*** Question 8 ***
*** Question 9 ***
*** Question 10 ***
*** Question 11 ***
*** Question 12 ***
*** Question 13 ***
