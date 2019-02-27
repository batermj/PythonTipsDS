.. _struct:

===============
Data Structures
===============

.. |nb| replace:: ``Jupyter Notebook``
.. |py| replace:: ``Python``
.. |pyc| replace:: ``:: Python Code:``
.. |out| replace:: ``:: Ouput:``
.. |eg| replace:: ``:: Example:``


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

Tuple
+++++

A tuple is an assortment of data, separated by commas, which makes it similar to the Python list, but a tuple is fundamentally different in that a tuple is "immutable." This means that it cannot be changed, modified, or manipulated.


[VanderPlas2016]_ [McKinney2013]_ [Georg2018]_