

.. _http://stsci.edu/schemas/asdf/core/complex-1.0.0:

complex: Complex number value.
==============================

:soft:`Type:` string ( :soft:`regex` :regexp:`([-+]?[0-9]*\\.?[0-9]+([eE][-+]?[0-9]+)?)?([-+][0-9]*\\.?[0-9]+([eE][-+]?[0-9]+)?[JjIi])?` ).

Complex number value.



Represents a complex number matching the following EBNF grammar

.. code:: 

   plus-or-minus = "+" | "-"
   suffix        = "J" | "j" | "I" | "i"
   complex       = [ieee754] [plus-or-minus ieee754 suffix]

Where :code:`ieee754` is a floating point number in IEEE 754 decimal
format.

Though :code:`J`, :code:`j`, :code:`I` and :code:`i` must be supported on reading, it is
recommended to use :code:`i` on writing.



:category:`Examples:`

1 real, -1 imaginary::

  !core/complex-1.0.0 1-1j

0 real, 1 imaginary::

  !core/complex-1.0.0 1J

-1 real, 0 imaginary::

  !core/complex-1.0.0 -1

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <complex-1.0.0.yaml>`
.. literalinclude:: complex-1.0.0.yaml
    :language: yaml
    :linenos:

