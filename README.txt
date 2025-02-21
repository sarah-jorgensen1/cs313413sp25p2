COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		There is no difference; all tests still run and take similar time to run.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			This method removes the value at the specified index from the list.

		list.remove(Integer.valueOf(5)); // what does this one do?

			This method removes the first instance of the specified value from the list.

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			An exception is thrown for concurrent modification, so the loop will not run successfully.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.
	These are examples of SIZEs you might choose, you can choose others if you wish.

	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:   65   38   39   39   67   38  ... (fill these in in ms)
        testLinkedListAddRemove:  74   35   59   36   32   61
		testArrayListAccess:      26   14   16   15   14   19
        testLinkedListAccess:     30   30   24   15   52   15

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:   98   52   52   89   51   50    ... (fill these in in ms)
        testLinkedListAddRemove:  63   35   35   28   52   60
		testArrayListAccess:      37   16   15   13   15   14
        testLinkedListAccess:     65   38   40   37   41   49

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  352  265  269  398  266  265  ... (fill these in in ms)
        testLinkedListAddRemove:  34   36   33   29   30   69
		testArrayListAccess:      14   20   30   20   16   20
        testLinkedListAccess:    722  655  656  655  761  652

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  3007 2641 2613 2642 2815 2644  ... (fill these in in ms)
        testLinkedListAddRemove:  54   30   31   31   38   32
		testArrayListAccess:      18   14   20   15   14   20
        testLinkedListAccess:    8730 8613 8543 8733 8591 8522

    SIZE 300000
    						            #1
    testArrayListAddRemove:           108000
    testLinkedListAddRemove:            130
    testArrayListAccess:                230
    testLinkedListAccess:             156000

	listAccess - which type of List is better to use, and why?

		ArrayLists are better for access because they take one step to access the value at a
		given index, but LinkedLists have to traverse every node before that element.

	listAddRemove - which type of List is better to use, and why?

		LinkedLists are better for adding and removing elements because it takes once step,
		linking a single node to a new node. In an ArrayList, a huge number of elements could
		all have to shift indices.