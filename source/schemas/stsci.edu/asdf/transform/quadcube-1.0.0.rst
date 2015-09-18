

.. _http://stsci.edu/schemas/asdf/transform/quadcube-1.0.0:

quadcube: Base class of all quadcube projections.
=================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

Base class of all quadcube projections.



Quadrilateralized spherical cube (quad-cube) projections belong to
the class of polyhedral projections in which the sphere is projected
onto the surface of an enclosing polyhedron.

The six faces of the quad-cube projections are numbered and laid out
as:

.. code:: 

         0
   4 3 2 1 4 3 2
         5



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/quadcube-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/quadcube-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/quadcube-1.0.0/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["pix2sky", "sky2pix"].

    

    

    :soft:`Default:` "pix2sky"

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <quadcube-1.0.0.yaml>`
.. literalinclude:: quadcube-1.0.0.yaml
    :language: yaml
    :linenos:

