.. _struct:

===============
Data Structures
===============

.. |nb| replace:: ``Jupyter Notebook``
.. |py| replace:: ``Python``
.. |pyc| replace:: ``:: Python Code:``
.. |out| replace:: ``:: Ouput:``
.. |eg| replace:: ``:: Example:``
.. |syn| replace:: ``::syntax:``


.. note::

	This Chapter :ref:`struct` is for beginner.  If you have some |py| programming experience, you may skip this chapter. 

List
++++

``List`` is one of data sctructures which is heavily using in my daily work. 

Create list
-----------

1. Create empty list

The empty list is used to initialize a list.  

|pyc|

	.. code-block:: python

		my_list = [] 
		type(my_list)

|out|

	.. code-block:: python

		list

I applied the empty list to initialize my ``silhouette score`` list when I try to find the 
optimal number of the clusters. 

|eg|

	.. code-block:: python

		min_cluster = 3
		max_cluster =8

		# silhouette_score
		scores = []

		for i in range(min_cluster, max_cluster):
		    score = np.round(np.random.random_sample(),2)
		    scores.append(score)

		print(scores)

|out|

	.. code-block:: python

		[0.16, 0.2, 0.3, 0.87, 0.59]



Unpack list
-----------

Methods of list objects
-----------------------

Methods of list objects:

+-----------------------------+-------------------------------------+
| Name                        |                      Description    |
+=============================+=====================================+
| list. ``append(x)``         | Add an item to the end of the list  |
+-----------------------------+-------------------------------------+
| list. ``extend(iterable)``  | Extend the list by appending all    |
+-----------------------------+-------------------------------------+
| list. ``insert(i, x)``      | Insert an item at a given position  |
+-----------------------------+-------------------------------------+
| list. ``remove(x)``         | Remove the first item               |
+-----------------------------+-------------------------------------+
| list. ``pop([i])``          | Remove the item at given position   |
+-----------------------------+-------------------------------------+
| list. ``clear()``           | Remove all items from the list      |
+-----------------------------+-------------------------------------+
| list. ``index(x[,s[,e]])``  | Return zero-based index in the list |
+-----------------------------+-------------------------------------+
| list. ``count(x)``          | Return the number of times x        |
+-----------------------------+-------------------------------------+
| list. ``sort(key,reverse)`` | Sort the items of the list          |
+-----------------------------+-------------------------------------+
| list. ``reverse()``         | Reverse the elements of the list    |
+-----------------------------+-------------------------------------+
| list. ``copy()``            | Return a shallow copy [#f1]_ of list|
+-----------------------------+-------------------------------------+

.. rubric:: Footnotes

.. [#f1] Shallow Copy vs Deep Copy Reference: https://stackoverflow.com/posts/184780/revisions

   Shallow copy:

   	.. figure:: images/shal.png 
    
   The variables A and B refer to different areas of memory, when B is assigned to A the two variables refer to the same area of memory. Later modifications to the contents of either are instantly reflected in the contents of other, as they share contents.

   Deep Copy:    

   	.. figure:: images/deep.png 

   The variables A and B refer to different areas of memory, when B is assigned to A the values in the memory area which A points to are copied into the memory area to which B points. Later modifications to the contents of either remain unique to A or B; the contents are not shared. 




Tuple
+++++

A tuple is an assortment of data, separated by commas, which makes it similar to the Python list, but a tuple is fundamentally different in that a tuple is "immutable." This means that it cannot be changed, modified, or manipulated.


Dictionary
++++++++++

One line if statement
+++++++++++++++++++++

1. With filter
--------------

|syn|

	.. code-block:: python

		[ EXP for x in seq if COND ]


|pyc|

	.. code-block:: python



|out|

	.. code-block:: python


2. Without filter
-----------------

|syn|

	.. code-block:: python

		[ EXP if COND RESUT else  RESUT for x in seq]


|pyc|

	.. code-block:: python



|out|

	.. code-block:: python

[VanderPlas2016]_ [McKinney2013]_ [Georg2018]_