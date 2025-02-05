Write Code Questions
---------------------

#.

    .. tabbed:: list_writeMyList

        .. tab:: Question

            Write a function called ``add_to_new_list`` that takes in a list of strings, ``lst``, as a parameter and creates a new list with the length 
            of ``lst`` and the first element of ``lst`` three times. For example, ``add_to_new_list(["1","2","3"])`` would return ``[3, '111']``.

            .. activecode:: list_writeMyListq

                def add_to_new_list(lst):
                    # write code here
                =====

                from unittest.gui import TestCaseGui

                class myTests(TestCaseGui):

                    def testOne(self):
                        self.assertEqual(add_to_new_list(['1','2','3']), [3, '111'], "add_to_new_list(['1','2','3'])")
                        self.assertEqual(add_to_new_list(['0','0','0','0']), [4, '000'], "add_to_new_list(['0','0','0','0'])")
                        self.assertEqual(add_to_new_list(['10.2','0.0','100','-2']), [4, '10.210.210.2'], "add_to_new_list(['10.2','0.0','100','-2'])")


                myTests().main()


        .. tab:: Answer

            .. activecode:: list_writeMyListA
                :optional:

                def add_to_new_list(lst):
                    new_list = []
                    new_list.append(len(lst))
                    new_list.append(lst[0] * 3)
                    return new_list

#.
    .. activecode::  list_writeItemsq
        :nocodelens:

        Write a function called ``item_lister`` that takes in a list of at least three values, ``items``, as a parameter. Set the first value to "First item", set 
        the second value to the first value previously set, and set the third value to its current value plus one (rounded to two decimals). (Note: the third value of ``items`` 
        will only be numerical.) Then, return the modified list. For example, ``itemLister([2,4,6,8])`` would return ``['First item', 'First item', 7, 8]``.
        ~~~~
        def itemLister(items):
            # write code here

        =====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(itemLister([2,4,6,8]), ['First item', 'First item', 7, 8], "itemLister([2,4,6,8])")
                self.assertEqual(itemLister([2.2,'hi',0]), ['First item', 'First item', 1], "itemLister([2.2,'hi',0])")
                self.assertEqual(itemLister([2.2,True,0]), ['First item', 'First item', 1], "itemLister([2.2,True,0])")
                self.assertEqual(itemLister([-2.2,'hi',-2.2]), ['First item', 'First item', -1.2], "itemLister([-2.2,'hi',-2.2])")

        myTests().main()

#.
    .. tabbed:: list_writeAvg

        .. tab:: Question

            Write a function called ``average`` that takes in a list of integers, ``aList``, as a parameter and returns the average of
            all of the integers, rounded to one decimal place. For example, ``average([99, 100, 74, 63, 100, 100])`` would return ``89.33``.

            .. activecode::  list_writeAvgq
                :nocodelens:

                def average(aList):
                    # write code here 
             
                =====

                from unittest.gui import TestCaseGui

                class myTests(TestCaseGui):

                    def testOne(self):
                        self.assertAlmostEqual(average([99, 100, 74, 63, 100, 100]), 89.3, 1, "average([99, 100, 74, 63, 100, 100])")
                        self.assertAlmostEqual(average([0, 2, -3, 1.2, 2000]), 400.0, 1, "average([0, 2, -3, 1.2, 2000])")
                        self.assertAlmostEqual(average([-2]), -2.0, 1, "average([-2])")


                myTests().main()


        .. tab:: Answer

            .. activecode:: list_writeAvgA
                :optional:

                def average(aList):
                    sum = 0
                    for num in aList:
                        sum += num
                    avg = round(sum / len(aList),2)
                    return avg

#.
    .. activecode:: list_write23q

        Write the function ``change_index3`` that takes in one parameter, ``lst``, and assigns the value at index 3 of ``lst`` to '200' and then returns ``lst``.
        For example, ``change_index3(['hi', 'goodbye', 'python', '106', '506'])`` would return ``['hi', 'goodbye', 'python', '200', '506']`` and 
        ``change_index3([1, 2, 0, -5, 4])`` would return ``[1, 2, 0, '200', 4]``.
        ~~~~
        def change_index3(lst):
            # write code here


        =====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(change_index3(['hi', 'goodbye', 'python', '106', '506']), ['hi', 'goodbye', 'python', '200', '506'], "change_index3(['hi', 'goodbye', 'python', '106', '506'])")
                self.assertEqual(change_index3([1, 2, 0, -5, 4]), [1, 2, 0, '200', 4], "change_index3([1, 2, 0, -5, 4])")
                self.assertEqual(change_index3([False, '2', 2.5, '200', -4]), [False, '2', 2.5, '200', -4], "change_index3([False, '2', 2.5, '200', -4]")


        myTests().main()

#.
    .. tabbed:: list_capitalize

        .. tab:: Question

            Write a function called ``capitalize`` that takes in a list of lists of strings, ``lst``, and makes the first letter of each element capitalized and adds 
            it to a new list and returns that new list. For example, ``capitalize([["hi"],["hello", "hey"]])`` would return ``['Hi', 'Hello', 'Hey']``.

            .. activecode:: list_capitalize_q

                def capitalize(lst):
                    # write code here
                  

                =====

                from unittest.gui import TestCaseGui

                class myTests(TestCaseGui):

                    def testOne(self):
                        self.assertEqual(capitalize([['hi'],['hello', 'hey']]), ['Hi', 'Hello', 'Hey'], "capitalize([['hi'],['hello', 'hey']])")
                        self.assertEqual(capitalize([['HI'],['HELLO', 'HEY']]), ['Hi', 'Hello', 'Hey'], "capitalize([['HI'],['HELLO', 'HEY']])")
                        self.assertEqual(capitalize([['go', 'blue'],['python', 'IS', 'The', 'Best']]), ['Go', 'Blue', 'Python', 'Is', 'The', 'Best'], "capitalize([['go', 'blue'],['python', 'IS', 'The', 'Best']])")

                myTests().main()

        .. tab:: Answer

            .. activecode:: list_capitalize_a
                :optional:

                def capitalize(lst):
                    new_list = []
                    for i in lst:
                        for j in i:
                            new_list.append(j.capitalize())
                    return new_list


#.
    .. activecode:: list_write5q

        Write a function called ``countWords`` that takes in a list, ``lst``, as a parameter, and returns the amount of words that have a length of 5.
        For example, ``countWords(['hello', 'hi', 'good morning', 'three', 'kitty']`` should return ``3``. 
        ~~~~
        def countWords(lst):
            # write code here

        ====
        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(countWords(['hello', 'hi', 'good morning', 'three', 'kitty']),3,"countWords(['hello', 'hi', 'good morning', 'three', 'kitty'])")
                self.assertEqual(countWords(['two', 'three', 'four', 'five', 'six', 'seven']),2,"countWords(['two', 'three', 'four', 'five', 'six', 'seven'])")
                self.assertEqual(countWords(['these', 'those', 'there']),3,"countWords(['these', 'those', 'there'])")
                self.assertEqual(countWords(['the', 'an', 'a']),0,"countWords(['the', 'an', 'a'])")


        myTests().main()

#.
    .. tabbed:: list_writeChop

        .. tab:: Question

            Write a function called ``chop`` that takes a list, ``lst``, and modifies it, removing the first and last elements.
            For example, ``chop([1,2,3,4,5]`` should return ``[2,3,4]``.

            .. activecode:: list_writeChopq

                def chop(lst):
                    # write code here


                =====

                from unittest.gui import TestCaseGui

                class myTests(TestCaseGui):

                    def testOne(self):
                        self.assertEqual(chop([1,2,3,4,5]),[2,3,4],"chop([1,2,3,4,5])")
                        self.assertEqual(chop([1,3,5,7,9,10]),[3,5,7,9],"chop([1,3,5,7,9,10])")
                        self.assertEqual(chop([2,9]),[],"chop([2,9])")

                myTests().main()

        .. tab:: Answer

            .. activecode:: list_writeChopa
                :optional:
                
                def chop(lst):
                    lst.pop(0)
                    lst.pop(-1)
                    return(lst)

#.
    .. activecode::  list_writeReverseq
        :nocodelens:

        Write a function called ``reverse`` that takes in one parameter, ``lst``, and returns the reverse of a passed list.  
        For example, ``reverse[1,2,3]`` should return ``[3, 2, 1]``.
        ~~~~
        def reverse(lst):
            # write code here
        ====
        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                  self.assertEqual(reverse([1,2,3,4,5]),[5,4,3,2,1],"reverse([1,2,3,4,5])")
                  self.assertEqual(reverse([1,3,5,7,9]),[9,7,5,3,1],"reverse([1,3,5,7,9])")
                  self.assertEqual(reverse([2,4,6,7,9]),[9,7,6,4,2],"reverse([2,4,6,7,9])")


        myTests().main()

#.
    .. tabbed:: list_writeSum

        .. tab:: Question

            Write a function called ``sumUntilEven`` that takes in one parameter, ``lst``, and returns the sum of all the 
            elements in the ``lst`` up to but not including the first even number. For example, ``sumUntilEven([1,2,3,4,5]``
            should return ``1`` and ``sumUntilEven([1,3,5,7,9]`` should return ``25``.

            .. activecode:: list_writeSumq

                def sumUntilEven(lst):
                    # write code here

                ====
                from unittest.gui import TestCaseGui

                class myTests(TestCaseGui):

                    def testOne(self):
                        self.assertEqual(sumUntilEven([1,2,3,4,5]),1,"sumUntilEven([1,2,3,4,5])")
                        self.assertEqual(sumUntilEven([1,3,5,7,9]),25,"sumUntilEven([1,3,5,7,9])")
                        self.assertEqual(sumUntilEven([2,4,6,7,9]),0,"sumUntilEven([2,4,6,7,9])")

                myTests().main()


        .. tab:: Answer

            .. activecode:: list_writeSuma
                :optional:

                def sumUntilEven(lst):
                    total = 0
                    element = 0
                    while element < len(lst) and lst[element] % 2 != 0:
                        total = total + lst[element]
                        element += 1
                    return total

#.
    .. activecode::  list_sortByLen
        :nocodelens:

        Write a function called ``sort_by_length`` that takes in one parameter, a list of strings, ``lst``, and returns the list sorted
        by the length of the strings. For example, ``sort_by_length(["hello", "hi", "hey", "greetings"])`` would return ``['hi', 'hey', 'hello', 'greetings']``.
        ~~~~
        def sort_by_length(lst):
            # write code here

        ====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                  self.assertEqual(sort_by_length(['hello', 'hi', 'hey', 'greetings']),['hi', 'hey', 'hello', 'greetings'],"sort_by_length(['hello', 'hi', 'hey', 'greetings'])")
                  self.assertEqual(sort_by_length(['hello', 'hello']),['hello', 'hello'],"sort_by_length(['hello', 'hello'])")
                  self.assertEqual(sort_by_length(['I', 'have', 'four', 'apples']),['I', 'have', 'four', 'apples'],"sort_by_length(['I', 'have', 'four', 'apples'])")

        myTests().main()
