

.. _http://stsci.edu/schemas/asdf/core/software-1.0.0:

software: Describes a software package.
=======================================

:soft:`Type:` object.

Describes a software package.





:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/core/software-1.0.0/properties/name:

  :entry:`name`

  :soft:`Type:` string. Required.

  

  The name of the application or library.
  
  



  .. _http://stsci.edu/schemas/asdf/core/software-1.0.0/properties/author:

  :entry:`author`

  :soft:`Type:` string. Required.

  

  The author (or institution) that produced the software package.
  
  



  .. _http://stsci.edu/schemas/asdf/core/software-1.0.0/properties/homepage:

  :entry:`homepage`

  :soft:`Type:` string ( :soft:`format` uri ). Required.

  

  A URI to the homepage of the software.
  
  



  .. _http://stsci.edu/schemas/asdf/core/software-1.0.0/properties/version:

  :entry:`version`

  :soft:`Type:` string. Required.

  

  The version of the software used.  It is recommended, but not
  required, that this follows the (Semantic Versioning
  Specification)[`http://semver.org/spec/v2.0.0.html <http://semver.org/spec/v2.0.0.html>`__].
  
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <software-1.0.0.yaml>`
.. literalinclude:: software-1.0.0.yaml
    :language: yaml
    :linenos:

