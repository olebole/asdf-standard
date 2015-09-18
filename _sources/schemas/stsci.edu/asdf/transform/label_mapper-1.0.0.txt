

.. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0:

label_mapper: Represents a mapping from a coordinate value to a label.
======================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

Represents a mapping from a coordinate value to a label.



A label mapper instance maps inputs to a label.  It is used together
with
:ref:`regions_selector <http://stsci.edu/schemas/asdf/transform/regions_selector-1.0.0>`. The
:ref:`label_mapper <http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0>`
returns the label corresponding to given inputs. The
:ref:`regions_selector <http://stsci.edu/schemas/asdf/transform/regions_selector-1.0.0>`
returns the transform corresponding to this label. This maps inputs
(e.g. pixels on a detector) to transforms uniquely.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper:

    :entry:`mapper`

    :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>` :soft:`or` object. Required.

    

    An array with the shape of the detector/observation.
    Pixel values are of type integer or string and represent
    region labels.
    Pixels which are not within any region have value 0 or " ".
    
    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/0:

      :entry:`—`

      :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>`.

      

      



      .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1:

      :entry:`—`

      :soft:`Type:` object.

      

      

      :category:`Properties:`



        .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1/properties/labels:

        :entry:`labels`

        :soft:`Type:` array :soft:`of` ( number :soft:`or` array :soft:`of` ( number ) ).

        

        

        :category:`Items:`



          .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1/properties/labels/items:

          :soft:`Type:` number :soft:`or` array :soft:`of` ( number ).

          

          

          :category:`Any of:`



            .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1/properties/labels/items/anyOf/0:

            :entry:`—`

            :soft:`Type:` number.

            

            



            .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1/properties/labels/items/anyOf/1:

            :entry:`—`

            :soft:`Type:` array :soft:`of` ( number ).

            

            

            :category:`Items:`



              .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1/properties/labels/items/anyOf/1/items:

              :soft:`Type:` number.

              

              



        .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1/properties/models:

        :entry:`models`

        :soft:`Type:` array :soft:`of` ( :doc:`transform-1.0.0 <transform-1.0.0>` ).

        

        

        :category:`Items:`



          .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/mapper/anyOf/1/properties/models/items:

          :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

          

          



    .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/inputs:

    :entry:`inputs`

    :soft:`Type:` array :soft:`of` ( string ).

    

    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/inputs/items:

      :soft:`Type:` string.

      

      



    .. _http://stsci.edu/schemas/asdf/transform/label_mapper-1.0.0/allOf/1/properties/inputs_mapping:

    :entry:`inputs_mapping`

    :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

    

    

:category:`Examples:`

Map array indices are to labels.::

  !transform/label_mapper-1.0.0
    mapper: !core/ndarray-1.0.0
      [[1, 0, 2],
      [1, 0, 2],
      [1, 0, 2]]
  

Map numbers dictionary to transforms which return labels.::

  !transform/label_mapper-1.0.0
    mapper: !!omap
    - !!omap
      labels: [-1.67833272, -1.9580548, -1.118888]
    - !!omap
      models:
    - !transform/compose-1.0.0
      forward:
      - !transform/remap_axes-1.0.0
        mapping: [1]
      - !transform/shift-1.0.0 {offset: 6.0}
    - !transform/compose-1.0.0
      forward:
      - !transform/remap_axes-1.0.0
        mapping: [1]
      - !transform/shift-1.0.0 {offset: 2.0}
    - !transform/compose-1.0.0
      forward:
      - !transform/remap_axes-1.0.0
        mapping: [1]
      - !transform/shift-1.0.0 {offset: 4.0}
    inputs: [x, y]
    inputs_mapping: !transform/remap_axes-1.0.0
      mapping: [0]
      n_inputs: 2
  

Map a number wihtin a range of numbers to transforms which return labels.::

  !transform/label_mapper-1.0.0
    mapper: !!omap
    - !!omap
      labels:
      - [3.2, 4.1]
      - [2.67, 2.98]
      - [1.95, 2.3]
    - !!omap
      models:
    - !transform/compose-1.0.0
      forward:
      - !transform/remap_axes-1.0.0
        mapping: [1]
      - !transform/shift-1.0.0 {offset: 6.0}
    - !transform/compose-1.0.0
      forward:
      - !transform/remap_axes-1.0.0
        mapping: [1]
      - !transform/shift-1.0.0 {offset: 2.0}
    - !transform/compose-1.0.0
      forward:
      - !transform/remap_axes-1.0.0
        mapping: [1]
      - !transform/shift-1.0.0 {offset: 4.0}
    inputs: [x, y]
    inputs_mapping: !transform/remap_axes-1.0.0
      mapping: [0]
      n_inputs: 2
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <label_mapper-1.0.0.yaml>`
.. literalinclude:: label_mapper-1.0.0.yaml
    :language: yaml
    :linenos:

