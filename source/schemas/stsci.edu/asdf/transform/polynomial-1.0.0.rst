

.. _http://stsci.edu/schemas/asdf/transform/polynomial-1.0.0:

polynomial: A Polynomial model.
===============================

:soft:`Type:` object.

A Polynomial model.



A polynomial model represented by its coefficients stored in
an ndarray of shape :math:`(n+1)` for univariate polynomials or :math:`(n+1, n+1)`
for polynomials with 2 variables, where :math:`n` is the highest total degree
of the polynomial.

.. math:: 

   P = \sum_{i, j=0}^{i+j=n}c_{ij} * x^{i} * y^{j}

Invertibility: This transform is not automatically invertible.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/transform/polynomial-1.0.0/properties/coefficients:

  :entry:`coefficients`

  :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>` :soft:`or` array. Required.

  

  An array with coefficients.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/transform/polynomial-1.0.0/properties/coefficients/anyOf/0:

    :entry:`—`

    :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>`.

    

    



    .. _http://stsci.edu/schemas/asdf/transform/polynomial-1.0.0/properties/coefficients/anyOf/1:

    :entry:`—`

    :soft:`Type:` array.

    

    

    :category:`Items:`

:category:`Examples:`

:math:`P = 1.2 + 0.3 * x + 56.1 * x^{2}`::

  !transform/polynomial-1.0.0
    coefficients: !core/ndarray-1.0.0
                    [1.2, 0.3, 56.1]
  

:math:`P = 1.2 + 0.3 * x + 3 * x * y + 2.1 * y^{2}`::

  !transform/polynomial-1.0.0
    coefficients: !core/ndarray-1.0.0
                    [[1.2, 0.0, 2.1],
                     [0.3, 3.0, 0.0],
                     [0.0, 0.0, 0.0]]
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <polynomial-1.0.0.yaml>`
.. literalinclude:: polynomial-1.0.0.yaml
    :language: yaml
    :linenos:

