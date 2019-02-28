.. _pdrdd:


====================================
``pd.DataFrame`` vs ``pd.DataFrame``  
====================================



.. |nb| replace:: ``Jupyter Notebook``
.. |zp| replace:: ``Zeppelin``
.. |py| replace:: ``Python``
.. |pyc| replace:: ``:: Python Code:``
.. |out| replace:: ``:: Ouput:``
.. |eg| replace:: ``:: Example:``
.. |comp| replace:: ``:: Comparison:``


.. .. note::

..	This Chapter :ref:`nb` is for beginner.  If you have some |py| programming experience, you may skip this chapter.


Create DataFrame
++++++++++++++++

From List
---------

.. code-block:: python

	my_list = [['a', 1, 2], ['b', 2, 3],['c', 3, 4]]
	col_name = ['A', 'B', 'C']

|pyc|

.. code-block:: python

	# caution for the columns=
	pd.DataFrame(my_list,columns= col_name)

	spark.createDataFrame(my_list, col_name).show()


|comp|

.. code-block:: python

	                  +---+---+---+
	                  |  A|  B|  C|
	   A  B  C        +---+---+---+
	0  a  1  2        |  a|  1|  2|
 	1  b  2  3        |  b|  2|  3|
 	2  c  3  4        |  c|  3|  4|
 	                  +---+---+---+

.. attention::

   Pay attentation to the parameter ``columns=`` in ``pd.DataFrame``. Since the default value will make the list as rows.


	|pyc|

	.. code-block:: python

		# caution for the columns=
		pd.DataFrame(my_list, columns= col_name)

		pd.DataFrame(my_list, col_name)


	|comp|

	.. code-block:: python

		   A  B  C             0  1  2	 	
		0  a  1  2          A  a  1  2
		1  b  2  3          B  b  2  3
		2  c  3  4          C  c  3  4

From Dict
---------

.. code-block:: python

	d = {'A': [0, 1, 0],
	     'B': [1, 0, 1],
	     'C': [1, 0, 0]}

|pyc|

.. code-block:: python

	pd.DataFrame(d)for 
	# Tedious for PySpark
 	spark.createDataFrame(np.array(list(d.values())).T.tolist(),list(d.keys())).show()

|comp|

.. code-block:: python

	                   +---+---+---+
	                   |  A|  B|  C|
	   A  B  C         +---+---+---+
	0  0  1  1         |  0|  1|  1|
	1  1  0  0         |  1|  0|  0|
	2  0  1  0         |  0|  1|  0|
	                   +---+---+---+

Load DataFrame
++++++++++++++

From ``.csv``
-------------


From ``.json``
--------------

Data from: http://api.luftdaten.info/static/v1/data.json

From DataBase
-------------

..

.. code-block:: python

	dp = pd.read_json("data/data.json")
	ds = spark.read.json('data/data.json')

|pyc|

.. code-block:: python

	dp[['id','timestamp']].head(4)
	ds[['id','timestamp']].show(4)

|comp|

.. code-block:: python

                                                    +----------+-------------------+
                                                    |        id|          timestamp|
                id  timestamp                       +----------+-------------------+
    0	2994551481  2019-02-28 17:23:52             |2994551481|2019-02-28 17:23:52|
    1	2994551482  2019-02-28 17:23:52             |2994551482|2019-02-28 17:23:52|
    2	2994551483  2019-02-28 17:23:52             |2994551483|2019-02-28 17:23:52|
    3	2994551484  2019-02-28 17:23:52             |2994551484|2019-02-28 17:23:52|
                                                    +----------+-------------------+
                                                    only showing top 4 rows


TODO..
------








.. ###################

.. code-block:: python



|pyc|

.. code-block:: python


|comp|

.. code-block:: python








