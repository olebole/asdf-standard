

.. _http://stsci.edu/schemas/asdf/transform/healpix-1.0.0:

healpix: HEALPix projection.
============================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

HEALPix projection.



Corresponds to the :code:`XPH` projection in the FITS WCS standard.

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/healpix-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/healpix-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/healpix-1.0.0/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["pix2sky", "sky2pix"].

    

    

    :soft:`Default:` "pix2sky"



    .. _http://stsci.edu/schemas/asdf/transform/healpix-1.0.0/allOf/1/properties/H:

    :entry:`H`

    :soft:`Type:` number.

    

    The number of facets in the longitude direction.
    
    

    :soft:`Default:` 4.0



    .. _http://stsci.edu/schemas/asdf/transform/healpix-1.0.0/allOf/1/properties/X:

    :entry:`X`

    :soft:`Type:` number.

    

    The number of facets in the latitude direction.
    
    

    :soft:`Default:` 3.0

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <healpix-1.0.0.yaml>`
.. literalinclude:: healpix-1.0.0.yaml
    :language: yaml
    :linenos:

