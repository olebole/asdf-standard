

.. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0:

frame: The base class of all coordinate frames.
===============================================

:soft:`Type:` object.

The base class of all coordinate frames.



These objects are designed to be nested in arbitrary ways to build up
transformation pipelines out of a number of low-level pieces.

Most of these coordinate frames are defined in `IERS
conventions <http://www.iers.org/IERS/EN/Publications/TechnicalNotes/tn36.html>`__.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/name:

  :entry:`name`

  :soft:`Type:` string. Required.

  

  A user-friendly name for the frame.
  
  



  .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/axes_order:

  :entry:`axes_order`

  :soft:`Type:` array :soft:`of` ( integer ).

  

  The order of the axes.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/axes_order/items:

    :soft:`Type:` integer.

    

    



  .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/axes_names:

  :entry:`axes_names`

  :soft:`Type:` array :soft:`of` ( string :soft:`or` null ).

  

  The name of each axis in this frame.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/axes_names/items:

    :soft:`Type:` string :soft:`or` null.

    

    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/axes_names/items/anyOf/0:

      :entry:`—`

      :soft:`Type:` string.

      

      



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/axes_names/items/anyOf/1:

      :entry:`—`

      :soft:`Type:` null.

      

      



  .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame:

  :entry:`reference_frame`

  :soft:`Type:` object.

  

  The reference frame.
  
  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/type:

    :entry:`type`

    :soft:`Type:` any :soft:`from` ["ICRS", "FK5", "FK4", "FK4_noeterms", "galactic", "galactocentric", "GCRS", "CIRS", "ITRS", "precessed_geocentric"]. Required.

    

    The reference frame type.  Some reference frame types
    require additional properties, listed next to each reference
    frame type below.
    
    The reference frames types are:
    
    -  :code:`ICRS`
    
    -  :code:`FK5`: :code:`equinox`.
    
    -  :code:`FK4`: :code:`equinox` and optionally :code:`obstime`.
    
    -  :code:`FK4_noeterms`: :code:`equinox` and optionally
       :code:`obstime`.
    
    -  :code:`galactic`
    
    -  :code:`galactocentric`: :code:`galcen_distance`, :code:`galcen_ra`,
       :code:`galcen_dec`, :code:`z_sun` and :code:`roll`.
    
    -  :code:`GCRS`: :code:`obstime`, :code:`obsgeoloc`, and
       :code:`obsgeovel`.
    
    -  :code:`CIRS`: :code:`obstime`.
    
    -  :code:`ITRS`: :code:`obstime`.
    
    -  :code:`precessed_geocentric`: :code:`obstime`, :code:`obsgeoloc`,
       and :code:`obsgeovel`.
    
    

    :soft:`Default:` "ICRS"



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/equinox:

    :entry:`equinox`

    :soft:`Type:` :doc:`time-1.0.0 <../time/time-1.0.0>`.

    

    The equinox of the reference frame.  Required when
    :code:`reference_frame` one of:
    
      :code:`FK5`, :code:`FK4`, :code:`FK4_noeterms`
    
    



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obstime:

    :entry:`obstime`

    :soft:`Type:` :doc:`time-1.0.0 <../time/time-1.0.0>`.

    

    The observation time of the reference frame, used to determine
    the location of the Earth.  Required when :code:`reference_frame` is
    one of:
    
      :code:`FK4`, :code:`FK4_noeterms`, :code:`GCRS`, :code:`CIRS`, :code:`ITRS`
    
    If not provided, it defaults to the same value as :code:`equinox`.
    
    



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_distance:

    :entry:`galcen_distance`

    :soft:`Type:` array.

    

    The distance from the Sun to the Galactic center.  Required when
    :code:`reference_frame` is :code:`galactocentric`.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_distance/0:

      :entry:`index[0]`

      :soft:`Type:` number.

      

      



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_distance/1:

      :entry:`index[1]`

      :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

      

      

      :soft:`Default:` "pc"



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_ra:

    :entry:`galcen_ra`

    :soft:`Type:` array.

    

    The Right Ascension (RA) of the Galactic center in the ICRS
    frame.  Required when :code:`reference_frame` is :code:`galactocentric`.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_ra/0:

      :entry:`index[0]`

      :soft:`Type:` number.

      

      



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_ra/1:

      :entry:`index[1]`

      :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

      

      

      :soft:`Default:` "deg"



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_dec:

    :entry:`galcen_dec`

    :soft:`Type:` array.

    

    The Declination (DEC) of the Galactic center in the ICRS frame.
    Required when :code:`reference_frame` is :code:`galactocentric`.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_dec/0:

      :entry:`index[0]`

      :soft:`Type:` number.

      

      



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/galcen_dec/1:

      :entry:`index[1]`

      :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

      

      

      :soft:`Default:` "deg"



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/z_sun:

    :entry:`z_sun`

    :soft:`Type:` array.

    

    The distance from the sun to the galactic midplane.  Required
    when :code:`reference_frame` is :code:`galactocentric`.  Required when
    :code:`reference_frame` is :code:`galactocentric`.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/z_sun/0:

      :entry:`index[0]`

      :soft:`Type:` number.

      

      



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/z_sun/1:

      :entry:`index[1]`

      :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

      

      

      :soft:`Default:` "pc"



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/roll:

    :entry:`roll`

    :soft:`Type:` array.

    

    The angle to rotate about the final x-axis, relative to the
    orientation for :code:`galactic`.  Required when :code:`reference_frame` is
    :code:`galactocentric`.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/roll/0:

      :entry:`index[0]`

      :soft:`Type:` number.

      

      



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/roll/1:

      :entry:`index[1]`

      :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

      

      

      :soft:`Default:` "deg"



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeoloc:

    :entry:`obsgeoloc`

    :soft:`Type:` array.

    

    3-vector giving the position of the observer relative to the
    center-of-mass of the Earth, oriented the same as
    BCRS/ICRS. Defaults to :code:`[0, 0, 0]`, meaning "true" GCRS.  Used
    when :code:`reference_frame` is :code:`GCRS` or :code:`precessed_geocentric`.
    
    

    :soft:`Default:` [[0, 0, 0]]

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeoloc/0:

      :entry:`index[0]`

      :soft:`Type:` array :soft:`of` ( number ) *len* = 3.

      

      

      :category:`Items:`



        .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeoloc/0/items:

        :soft:`Type:` number.

        

        



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeoloc/1:

      :entry:`index[1]`

      :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

      

      

      :soft:`Default:` "m"



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeovel:

    :entry:`obsgeovel`

    :soft:`Type:` array.

    

    3-vector giving the velocity of the observer relative to the
    center-of-mass of the Earth, oriented the same as
    BCRS/ICRS. Defaults to :code:`[0, 0, 0]`, meaning "true" GCRS.  Used
    when :code:`reference_frame` is :code:`GCRS` or :code:`precessed_geocentric`.
    
    

    :soft:`Default:` [[0, 0, 0]]

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeovel/0:

      :entry:`index[0]`

      :soft:`Type:` array :soft:`of` ( number ) *len* = 3.

      

      

      :category:`Items:`



        .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeovel/0/items:

        :soft:`Type:` number.

        

        



      .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/reference_frame/properties/obsgeovel/1:

      :entry:`index[1]`

      :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

      

      

      :soft:`Default:` "m/s"



  .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/unit:

  :entry:`unit`

  :soft:`Type:` array :soft:`of` ( :doc:`unit-1.0.0 <../unit/unit-1.0.0>` ).

  

  Units for each axis.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/wcs/frame-1.0.0/properties/unit/items:

    :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

    

    

:category:`Examples:`

A celestial frame in the FK4 reference frame.
::

  !wcs/celestial_frame-1.0.0
    axes_names: [ra, dec]
    name: CelestialFrame
    reference_frame:
      type: FK4
      equinox: !time/time-1.0.0 '2010-01-01 00:00:00.000'
      obstime: !time/time-1.0.0 '2015-01-01 00:00:00.000'
    unit: [!unit/unit-1.0.0 deg, !unit/unit-1.0.0 deg]
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <frame-1.0.0.yaml>`
.. literalinclude:: frame-1.0.0.yaml
    :language: yaml
    :linenos:

