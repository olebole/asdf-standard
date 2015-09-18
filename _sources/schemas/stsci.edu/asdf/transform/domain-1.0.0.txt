

.. _http://stsci.edu/schemas/asdf/transform/domain-1.0.0:

domain: Defines the domain of an input axis.
============================================

:soft:`Type:` any.

Defines the domain of an input axis.



Describes the range of acceptable input values to a particular axis of a transform.



:category:`Examples:`

The domain :code:`[0, 1)`.::

  !transform/domain-1.0.0
    lower: 0
    upper: 1
    includes_lower: true
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <domain-1.0.0.yaml>`
.. literalinclude:: domain-1.0.0.yaml
    :language: yaml
    :linenos:

