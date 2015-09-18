

.. _http://stsci.edu/schemas/asdf/time/time-1.0.0:

time: Represents an instance in time.
=====================================

:soft:`Type:` any :soft:`and` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>` :soft:`or` :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>` :soft:`or` object :soft:`or` object.

Represents an instance in time.



A "time" is a single instant in time.  It may explicitly specify the
way time is represented (the "format") and the "scale" which
specifies the offset and scaling relation of the unit of time.

Specific emphasis is placed on supporting time scales (e.g. UTC,
TAI, UT1, TDB) and time representations (e.g. JD, MJD, ISO 8601)
that are used in astronomy and required to calculate, e.g., sidereal
times and barycentric corrections.

Times may be represented as one of the following:

-  an object, with explicit :code:`value`, and optional
   :code:`format`, :code:`scale` and :code:`location`.

-  a string, in which case the format is guessed from across the
   unambiguous options (:code:`iso`, :code:`byear`, :code:`jyear`,
   :code:`yday`), and the scale is hardcoded to :code:`UTC`.

In either case, a single time tag may be used to represent an
n-dimensional array of times, using either an :code:`ndarray` tag or
inline as (possibly nested) YAML lists.  If YAML lists, the same
format must be used for all time values.

The precision of the numeric formats should only be assumed to be as
good as an IEEE-754 double precision (float64) value.  If
higher-precision is required, the :code:`iso` or :code:`yday` format should be
used.



:category:`Definitions:`



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/iso_time:

  :entry:`iso_time`

  :soft:`Type:` string ( :soft:`regex` :regexp:`[0-9]{4}-(0[1-9])|(1[0-2])-(0[1-9])|([1-2][0-9])|(3[0-1])[T ]([0-1][0-9])|(2[0-4]):[0-5][0-9]:[0-5][0-9](.[0-9]+)?` ).

  

  



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/byear:

  :entry:`byear`

  :soft:`Type:` string ( :soft:`regex` :regexp:`B[0-9]+(.[0-9]+)?` ).

  

  



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/jyear:

  :entry:`jyear`

  :soft:`Type:` string ( :soft:`regex` :regexp:`J[0-9]+(.[0-9]+)?` ).

  

  



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/yday:

  :entry:`yday`

  :soft:`Type:` string ( :soft:`regex` :regexp:`[0-9]{4}:(00[1-9])|(0[1-9][0-9])|([1-2][0-9][0-9])|(3[0-5][0-9])|(36[0-5]):([0-1][0-9])|([0-1][0-9])|(2[0-4]):[0-5][0-9]:[0-5][0-9](.[0-9]+)?` ).

  

  



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats:

  :entry:`string_formats`

  :soft:`Type:` :ref:`definitions/iso_time <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/iso_time>` :soft:`or` :ref:`definitions/byear <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/byear>` :soft:`or` :ref:`definitions/jyear <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/jyear>` :soft:`or` :ref:`definitions/yday <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/yday>`.

  

  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats/anyOf/0:

    :entry:`—`

    :soft:`Type:` :ref:`definitions/iso_time <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/iso_time>`.

    

    



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats/anyOf/1:

    :entry:`—`

    :soft:`Type:` :ref:`definitions/byear <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/byear>`.

    

    



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats/anyOf/2:

    :entry:`—`

    :soft:`Type:` :ref:`definitions/jyear <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/jyear>`.

    

    



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats/anyOf/3:

    :entry:`—`

    :soft:`Type:` :ref:`definitions/yday <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/yday>`.

    

    



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings:

  :entry:`array_of_strings`

  :soft:`Type:` array :soft:`of` ( :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>` :soft:`or` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>` ).

  

  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings/items:

    :soft:`Type:` :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>` :soft:`or` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>`.

    

    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings/items/anyOf/0:

      :entry:`—`

      :soft:`Type:` :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>`.

      

      



      .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings/items/anyOf/1:

      :entry:`—`

      :soft:`Type:` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>`.

      

      

:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` any.

  

  



  .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>` :soft:`or` :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>` :soft:`or` object :soft:`or` object.

  

  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/0:

    :entry:`—`

    :soft:`Type:` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>`.

    

    



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/1:

    :entry:`—`

    :soft:`Type:` :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>`.

    

    



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/2:

    :entry:`—`

    :soft:`Type:` object.

    

    

    :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3:

    :entry:`—`

    :soft:`Type:` object.

    

    

    :category:`Properties:`



      .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/value:

      :entry:`value`

      :soft:`Type:` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>` :soft:`or` :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>` :soft:`or` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>` :soft:`or` number. Required.

      

      The value(s) of the time.
      
      

      :category:`Any of:`



        .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/value/anyOf/0:

        :entry:`—`

        :soft:`Type:` :ref:`definitions/string_formats <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/string_formats>`.

        

        



        .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/value/anyOf/1:

        :entry:`—`

        :soft:`Type:` :ref:`definitions/array_of_strings <http://stsci.edu/schemas/asdf/time/time-1.0.0/definitions/array_of_strings>`.

        

        



        .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/value/anyOf/2:

        :entry:`—`

        :soft:`Type:` :doc:`ndarray-1.0.0 <../core/ndarray-1.0.0>`.

        

        



        .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/value/anyOf/3:

        :entry:`—`

        :soft:`Type:` number.

        

        



      .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/format:

      :entry:`format`

      :soft:`Type:` any :soft:`from` ["iso", "yday", "byear", "jyear", "decimalyear", "jd", "mjd", "gps", "unix", "cxcsec"].

      

      The format of the time.
      
      If not provided, the the format should be guessed from the
      string from among the following unambiguous options:
      :code:`iso`, :code:`byear`, :code:`jyear` and :code:`yday`.
      
      The supported formats are:
      
      -  :code:`iso`: ISO 8601 compliant date-time format :code:`YYYY-MM-
         DDTHH:MM:SS.sss...`.  For example, :code:`2000-01-01 00:00:00.000`
         is midnight on January 1,   #. The :code:`T` separating the date
         from the time section is    optional.
      
      -  :code:`yday`: Year, day-of-year and time as
         :code:`YYYY:DOY:HH:MM:SS.sss...`. The day-of-year (DOY) goes from
         001 to 365 (366 in leap years). For example,
         :code:`2000:001:00:00:00.000` is midnight on January 1, 2000.
      
      -  :code:`byear`: Besselian Epoch year, eg. :code:`B1950.0`.  The
         :code:`B` is optional if the :code:`byear` format is explicitly
         specified.
      
      -  :code:`jyear`: Julian Epoch year, eg. :code:`J2000.0`.  The
         :code:`J` is optional if the :code:`jyear` format is explicitly
         specified.
      
      -  :code:`decimalyear`: Time as a decimal year, with integer values
         corresponding to midnight of the first day of each year. For
         example 2000.5 corresponds to the ISO time :code:`2000-07-02
         00:00:00`.
      
      -  :code:`jd`: Julian Date time format. This represents the number of
         days since the beginning of the Julian Period. For example,
         2451544.5 in :code:`jd` is midnight on January 1, 2000.
      
      -  :code:`mjd`: Modified Julian Date time format. This represents the
         number of days since midnight on November 17, 1858. For example,
         51544.0 in MJD is midnight on January 1, 2000.
      
      -  :code:`gps`: GPS time: seconds from 1980-01-06 00:00:00 UTC For
         example, 630720013.0 is midnight on January 1, 2000.
      
      -  :code:`unix`: Unix time: seconds from 1970-01-01 00:00:00 UTC. For
         example, 946684800.0 in Unix time is midnight on January 1, 2000.
         [TODO: Astropy's definition of UNIX time doesn't match POSIX's
         here.  What should we do for the purposes of ASDF?]
      
      



      .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/scale:

      :entry:`scale`

      :soft:`Type:` any :soft:`from` ["utc", "tai", "tcb", "tcg", "tdb", "tt", "ut1"].

      

      The time scale (or time standard) is a specification for
      measuring time: either the rate at which time passes; or
      points in time; or both. See also [3] and [4].
      
      These scales are defined in detail in `SOFA Time Scale and
      Calendar Tools <http://www.iausofa.org/sofa_ts_c.pdf>`__.
      
      The supported time scales are:
      
      -  :code:`utc`: Coordinated Universal Time (UTC).  This is the default
         time scale, except for :code:`gps`, :code:`unix`.
      
      -  :code:`tai`: International Atomic Time (TAI).
      
      -  :code:`tcb`: Barycentric Coordinate Time (TCB).
      
      -  :code:`tcg`: Geocentric Coordinate Time (TCG).
      
      -  :code:`tdb`: Barycentric Dynamical Time (TDB).
      
      -  :code:`tt`: Terrestrial Time (TT).
      
      -  :code:`ut1`: Universal Time (UT1).
      
      



      .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location:

      :entry:`location`

      :soft:`Type:` object :soft:`or` object.

      

      Specifies the observer location for scales that are
      sensitive to observer location, currently only :code:`tdb`.  May
      be specified either with geocentric coordinates (X, Y, Z)
      with an optional unit or geodetic coordinates:
      
      -  :code:`long`: longitude in degrees
      
      -  :code:`lat`: in degrees
      
      -  :code:`h`: optional height
      
      

      :category:`Any of:`



        .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/0:

        :entry:`—`

        :soft:`Type:` object.

        

        

        :category:`Properties:`



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/0/properties/x:

          :entry:`x`

          :soft:`Type:` number. Required.

          

          



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/0/properties/y:

          :entry:`y`

          :soft:`Type:` number. Required.

          

          



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/0/properties/z:

          :entry:`z`

          :soft:`Type:` number. Required.

          

          



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/0/properties/unit:

          :entry:`unit`

          :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>` :soft:`and` any.

          

          

          :category:`All of:`



            .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/0/properties/unit/allOf/0:

            :entry:`0`

            :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

            

            



            .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/0/properties/unit/allOf/1:

            :entry:`1`

            :soft:`Type:` any.

            

            

            :soft:`Default:` "m"



        .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/1:

        :entry:`—`

        :soft:`Type:` object.

        

        

        :category:`Properties:`



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/1/properties/long:

          :entry:`long`

          :soft:`Type:` number -180 ≤ *x* ≤ 180. Required.

          

          



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/1/properties/lat:

          :entry:`lat`

          :soft:`Type:` number -90 ≤ *x* ≤ 90. Required.

          

          



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/1/properties/h:

          :entry:`h`

          :soft:`Type:` number.

          

          

          :soft:`Default:` 0



          .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/1/properties/unit:

          :entry:`unit`

          :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>` :soft:`and` any.

          

          

          :category:`All of:`



            .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/1/properties/unit/allOf/0:

            :entry:`0`

            :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

            

            



            .. _http://stsci.edu/schemas/asdf/time/time-1.0.0/allOf/1/anyOf/3/properties/location/anyOf/1/properties/unit/allOf/1:

            :entry:`1`

            :soft:`Type:` any.

            

            

            :soft:`Default:` "m"

:category:`Examples:`

Example ISO time::

  !time/time-1.0.0 "2000-12-31T13:05:27.737"
  

Example year, day-of-year and time format time::

  !time/time-1.0.0 "2001:003:04:05:06.789"
  

Example Besselian Epoch time::

  !time/time-1.0.0 B2000.0
  

Example Besselian Epoch time, equivalent to above::

  !time/time-1.0.0
    value: 2000.0
    format: byear
  

Example list of times::

  !time/time-1.0.0
    ["2000-12-31T13:05:27.737", "2000-12-31T13:06:38.444"]
  

Example of an array of times::

  !time/time-1.0.0
    value: !core/ndarray-1.0.0
      data: [2000, 2001]
      datatype: float64
    format: jyear
  

Example with a location::

  !time/time-1.0.0
    value: 2000.0
    format: jyear
    scale: tdb
    location:
      x: 6378100
      y: 0
      z: 0
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <time-1.0.0.yaml>`
.. literalinclude:: time-1.0.0.yaml
    :language: yaml
    :linenos:

