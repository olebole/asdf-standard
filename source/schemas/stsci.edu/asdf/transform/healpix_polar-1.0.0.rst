

.. _http://stsci.edu/schemas/asdf/transform/healpix_polar-1.0.0:

healpix_polar: HEALPix polar, aka "butterfly", projection.
==========================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

HEALPix polar, aka "butterfly", projection.



Corresponds to the :code:`XPH` projection in the FITS WCS standard.

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/healpix_polar-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/healpix_polar-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/healpix_polar-1.0.0/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["pix2sky", "sky2pix"].

    

    

    :soft:`Default:` "pix2sky"

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <healpix_polar-1.0.0.yaml>`
.. literalinclude:: healpix_polar-1.0.0.yaml
    :language: yaml
    :linenos:

