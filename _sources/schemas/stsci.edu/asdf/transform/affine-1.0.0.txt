

.. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0:

affine: An affine transform.
============================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

An affine transform.



Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/matrix:

    :entry:`matrix`

    :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>` :soft:`or` array :soft:`of` ( array :soft:`of` ( number ) *len* = 2 ) *len* = 2. Required.

    

    An array of size (*n* x *n*), where *n* is the number of axes,
    representing the linear transformation in an affine transform.
    
    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/matrix/anyOf/0:

      :entry:`—`

      :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>`.

      

      



      .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/matrix/anyOf/1:

      :entry:`—`

      :soft:`Type:` array :soft:`of` ( array :soft:`of` ( number ) *len* = 2 ) *len* = 2.

      

      

      :category:`Items:`



        .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/matrix/anyOf/1/items:

        :soft:`Type:` array :soft:`of` ( number ) *len* = 2.

        

        

        :category:`Items:`



          .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/matrix/anyOf/1/items/items:

          :soft:`Type:` number.

          

          



    .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/translation:

    :entry:`translation`

    :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>` :soft:`or` array :soft:`of` ( number ) *len* = 2.

    

    An array of size (*n*,), where  *n* is the number of axes,
    representing the translation in an affine transform.
    
    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/translation/anyOf/0:

      :entry:`—`

      :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>`.

      

      



      .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/translation/anyOf/1:

      :entry:`—`

      :soft:`Type:` array :soft:`of` ( number ) *len* = 2.

      

      

      :category:`Items:`



        .. _http://stsci.edu/schemas/asdf/transform/affine-1.0.0/allOf/1/properties/translation/anyOf/1/items:

        :soft:`Type:` number.

        

        

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <affine-1.0.0.yaml>`
.. literalinclude:: affine-1.0.0.yaml
    :language: yaml
    :linenos:

