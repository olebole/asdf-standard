

.. _http://stsci.edu/schemas/asdf/transform/rotate3d-1.0.0:

rotate3d: Rotation in 3D space.
===============================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

Rotation in 3D space.



Euler angle rotation around 3 axes.

Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/rotate3d-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/rotate3d-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/rotate3d-1.0.0/allOf/1/properties/phi:

    :entry:`phi`

    :soft:`Type:` number. Required.

    

    Angle, in degrees.
    
    



    .. _http://stsci.edu/schemas/asdf/transform/rotate3d-1.0.0/allOf/1/properties/theta:

    :entry:`theta`

    :soft:`Type:` number. Required.

    

    Angle, in degrees.
    
    



    .. _http://stsci.edu/schemas/asdf/transform/rotate3d-1.0.0/allOf/1/properties/psi:

    :entry:`psi`

    :soft:`Type:` number. Required.

    

    Angle, in degrees.
    
    



    .. _http://stsci.edu/schemas/asdf/transform/rotate3d-1.0.0/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["zxz", "zyz", "yzy", "yxy", "xyx", "xzx", "native2celestial", "celestial2native"]. Required.

    

    Sequence of rotation axes: one of :code:`zxz`, :code:`zyz`, :code:`yzy`, :code:`yxy`, :code:`xyx`, :code:`xzx`
    or :code:`native2celestial`, :code:`celestial2native`.
    
    If :code:`direction` is :code:`native2celestial` or :code:`celestial2native`,
    :code:`phi`, :code:`theta` are the longitude and latitude of the native pole in
    the celestial system and :code:`psi` is the longitude of the celestial pole in
    the native system.
    
    

    :soft:`Default:` "native2celestial"

:category:`Examples:`

The three Euler angles are 12.3, 34 and -1.2 in degrees.::

  !transform/rotate3d-1.0.0
    phi: 12.3
    theta: 34
    psi: -1.2
    direction: zxz
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <rotate3d-1.0.0.yaml>`
.. literalinclude:: rotate3d-1.0.0.yaml
    :language: yaml
    :linenos:

