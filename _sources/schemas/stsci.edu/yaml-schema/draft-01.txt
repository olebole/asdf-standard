

.. _http://stsci.edu/schemas/yaml-schema/draft-01:

draft: YAML Schema
==================

:soft:`Type:` `schema <http://json-schema.org/draft-04/schema>`__ :soft:`and` object.

YAML Schema



A metaschema extending JSON Schema's metaschema to add support for
some YAML-specific constructions.



:category:`All of:`



  .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/0:

  :entry:`0`

  :soft:`Type:` `schema <http://json-schema.org/draft-04/schema>`__.

  

  



  .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/tag:

    :entry:`tag`

    :soft:`Type:` string ( *len* ≥ 6 ).

    

    A fully-qualified YAML tag name that should be associated
    with the object type returned by the YAML parser; for
    example, the object must be an instance of the class
    registered with the parser to create instances of objects
    with this tag. Implementation of this validator is optional
    and depends on details of the YAML parser.
    
    



    .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/propertyOrder:

    :entry:`propertyOrder`

    :soft:`Type:` array :soft:`of` ( string ).

    

    Specifies the default order of the properties when writing
    out.  Any keys not listed in propertyOrder will be in
    arbitrary order at the end.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/propertyOrder/items:

      :soft:`Type:` string.

      

      



    .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/flowStyle:

    :entry:`flowStyle`

    :soft:`Type:` string :soft:`from` ["block", "flow"].

    

    Specifies the default serialization style to use for an
    array or object.  YAML supports multiple styles for
    arrays/sequences and objects/maps, called "block style" and
    "flow style".  For example::
    
      Block style: !!map
        Clark : Evans
        Ingy  : döt Net
        Oren  : Ben-Kiki
    
      Flow style: !!map { Clark: Evans, Ingy: döt Net, Oren: Ben-Kiki }
    
    This property gives a hint to the tool outputting the YAML
    which style to use.  If not provided, the library is free to
    use whatever heuristics it wishes to determine the output
    style.  This property does not enforce any particular style
    on YAML being parsed.
    
    



    .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/style:

    :entry:`style`

    :soft:`Type:` string :soft:`from` ["inline", "literal", "folded"].

    

    Specifies the default serialization style to use for a string.
    YAML supports multiple styles for strings::
    
      Inline style: "First line\nSecond line"
    
      Literal style: |
        First line
        Second line
    
      Folded style: >
        First
        line
    
    .. code:: 
    
       Second
       line
    
    This property gives a hint to the tool outputting the YAML
    which style to use.  If not provided, the library is free to
    use whatever heuristics it wishes to determine the output
    style.  This property does not enforce any particular style
    on YAML being parsed.
    
    



    .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/examples:

    :entry:`examples`

    :soft:`Type:` array :soft:`of` ( array ).

    

    A list of examples to help document the schema.  Each pair
    is a prose description followed by a string containing YAML
    content.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/examples/items:

      :soft:`Type:` array.

      

      

      :category:`Items:`



        .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/examples/items/0:

        :entry:`index[0]`

        :soft:`Type:` string.

        

        



        .. _http://stsci.edu/schemas/yaml-schema/draft-01/allOf/1/properties/examples/items/1:

        :entry:`index[1]`

        :soft:`Type:` string.

        

        

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <draft-01.yaml>`
.. literalinclude:: draft-01.yaml
    :language: yaml
    :linenos:

