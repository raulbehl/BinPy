
Example for Half Adder class.
-----------------------------

.. code:: python

    # Imports
    
    from __future__ import print_function
    from BinPy.combinational.combinational import *
.. code:: python

    # Initializing the HalfAdder class
    
    ha = HalfAdder(0, 1)
    
    # Output of HalfAdder
    
    print (ha.output())

.. parsed-literal::

    [0, 1]


.. code:: python

    # The output is of the form [SUM, CARRY]"
    
    # Input changes
    
    # Input at index 1 is changed to 0
    
    ha.set_input(1, 0)
    
    # New Output of the HalfAdder
    
    print (ha.output())

.. parsed-literal::

    [0, 0]


.. code:: python

    # Changing the number of inputs
    
    # No need to set the number, just change the inputs
    
    # Input length must be two
    
    ha.set_inputs(1, 1)
.. code:: python

    # New output of HalfAdder
    
    print (ha.output())

.. parsed-literal::

    [1, 0]


.. code:: python

    # Using Connectors as the input lines
    
    # Take a Connector
    
    conn = Connector()
    
    # Set Output at index to Connector conn
    
    ha.set_output(0, conn)
    
    # Put this connector as the input to gate1
    
    gate1 = AND(conn, 0)
    
    # Output of the gate1
    
    print (gate1.output())

.. parsed-literal::

    0

