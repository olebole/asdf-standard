

.. _http://stsci.edu/schemas/asdf/core/asdf-1.0.0:

asdf: Top-level schema for every ASDF file.
===========================================

:soft:`Type:` object.

Top-level schema for every ASDF file.



This schema contains the top-level attributes for every ASDF file.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/core/asdf-1.0.0/properties/asdf_library:

  :entry:`asdf_library`

  :soft:`Type:` :doc:`software-1.0.0 <software-1.0.0>`.

  

  Describes the ASDF library that produced the file.
  
  



  .. _http://stsci.edu/schemas/asdf/core/asdf-1.0.0/properties/history:

  :entry:`history`

  :soft:`Type:` array :soft:`of` ( :doc:`history_entry-1.0.0 <history_entry-1.0.0>` ).

  

  A log of transformations that have happened to the file.  May
  include such things as data collection, data calibration
  pipelines, data analysis etc.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/core/asdf-1.0.0/properties/history/items:

    :soft:`Type:` :doc:`history_entry-1.0.0 <history_entry-1.0.0>`.

    

    



  .. _http://stsci.edu/schemas/asdf/core/asdf-1.0.0/properties/data:

  :entry:`data`

  :soft:`Type:` :doc:`ndarray-1.0.0 <ndarray-1.0.0>`.

  

  The data array corresponds to the main science data array in the
  file.  Oftentimes, the data model will be much more complex than
  a single array, but this array will be used by applications that
  just want to convert to a display an image or preview of the
  file.  It is recommended, but not required, that it is a
  2-dimensional image array.
  
  



  .. _http://stsci.edu/schemas/asdf/core/asdf-1.0.0/properties/fits:

  :entry:`fits`

  :soft:`Type:` :doc:`fits-1.0.0 <../fits/fits-1.0.0>`.

  

  A way to specify exactly how this ASDF file should be converted
  to FITS.
  
  



  .. _http://stsci.edu/schemas/asdf/core/asdf-1.0.0/properties/wcs:

  :entry:`wcs`

  :soft:`Type:` :doc:`wcs-1.0.0 <../wcs/wcs-1.0.0>`.

  

  The location of the main WCS for the main data.
  
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <asdf-1.0.0.yaml>`
.. literalinclude:: asdf-1.0.0.yaml
    :language: yaml
    :linenos:

