

.. _http://stsci.edu/schemas/asdf/transform/airy-1.0.0:

airy: The Airy projection.
==========================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>` :soft:`and` object.

The Airy projection.



Corresponds to the :code:`AIR` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0>`
for the definition of the full transformation.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/airy-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/airy-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/airy-1.0.0/allOf/1/properties/theta_b:

    :entry:`theta_b`

    :soft:`Type:` number.

    

    The latitude :math:`\theta_b` at which to minimize the error, in
    degrees.
    
    

    :soft:`Default:` 90

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <airy-1.0.0.yaml>`
.. literalinclude:: airy-1.0.0.yaml
    :language: yaml
    :linenos:

