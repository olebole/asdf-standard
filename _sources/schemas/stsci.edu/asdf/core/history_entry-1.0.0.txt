

.. _http://stsci.edu/schemas/asdf/core/history_entry-1.0.0:

history_entry: An entry in the file history.
============================================

:soft:`Type:` object.

An entry in the file history.





:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/core/history_entry-1.0.0/properties/description:

  :entry:`description`

  :soft:`Type:` string.

  

  A description of the transformation performed.
  
  



  .. _http://stsci.edu/schemas/asdf/core/history_entry-1.0.0/properties/time:

  :entry:`time`

  :soft:`Type:` string ( :soft:`format` date-time ).

  

  A timestamp for the operation, in UTC.
  
  



  .. _http://stsci.edu/schemas/asdf/core/history_entry-1.0.0/properties/software:

  :entry:`software`

  :soft:`Type:` :doc:`software-1.0.0 <software-1.0.0>` :soft:`or` array :soft:`of` ( :doc:`software-1.0.0 <software-1.0.0>` ).

  

  One or more descriptions of the software that performed the
  operation.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/core/history_entry-1.0.0/properties/software/anyOf/0:

    :entry:`—`

    :soft:`Type:` :doc:`software-1.0.0 <software-1.0.0>`.

    

    



    .. _http://stsci.edu/schemas/asdf/core/history_entry-1.0.0/properties/software/anyOf/1:

    :entry:`—`

    :soft:`Type:` array :soft:`of` ( :doc:`software-1.0.0 <software-1.0.0>` ).

    

    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/core/history_entry-1.0.0/properties/software/anyOf/1/items:

      :soft:`Type:` :doc:`software-1.0.0 <software-1.0.0>`.

      

      

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <history_entry-1.0.0.yaml>`
.. literalinclude:: history_entry-1.0.0.yaml
    :language: yaml
    :linenos:

