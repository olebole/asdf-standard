

.. _http://stsci.edu/schemas/asdf/unit/unit-1.0.0:

unit: Physical unit.
====================

:soft:`Type:` any :soft:`or` any.

Physical unit.



This represents a physical unit, in `VOUnit syntax, Version 1.0 <http://www.ivoa.net/documents/VOUnits/index.html>`__.
Where units are not explicitly tagged, they are assumed to be in VOUnit syntax.



:category:`Any of:`



  .. _http://stsci.edu/schemas/asdf/unit/unit-1.0.0/anyOf/0:

  :entry:`—`

  :soft:`Type:` any.

  

  



  .. _http://stsci.edu/schemas/asdf/unit/unit-1.0.0/anyOf/1:

  :entry:`—`

  :soft:`Type:` any.

  

  

:category:`Examples:`

Example unit::

  !unit/unit-1.0.0 "2.1798721 10-18kg m2 s-2"
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <unit-1.0.0.yaml>`
.. literalinclude:: unit-1.0.0.yaml
    :language: yaml
    :linenos:

