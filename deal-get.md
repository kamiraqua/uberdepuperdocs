URL:
----
[http://api.feest.je/1/deal/get](http://api.feest.je/1/deal/get)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
False, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call returns an array filled with deals. Depending on the parameters.

PARAMETERS:
-----------

**Required:**

 - None
 
**Optional:**

 - **lat**(*float*), returns deals at the given geolocation. Requires lng.
 - **lng**(*float*), returns deals at the given geolocation. Requires lat.
 - **sort**(*string*), if start, sorts deals by the starting time, if end, sorts deals by ending time, AANVULLEN
 - **deal**(*string*), returns the deal with the given *dealid*.
 - **highlighted**(*bool*), if true, returns highlighted deals only, if false, returns non highlighted deals only, if other, returns all deals
 - **spot**(*string*), returns deals at the spot with the given *spotid*.

**Extra:**

 - None

RESPONSE FIELDS:
----------------

 - **_id**, shows the id of the deal.
 - **name**, shows the name of the deal.
 - **nameslug**, shows the nameslug of the deal.
 - **highlighted**, shows whether the deal is highlighted or not.
 - **hasphoto**, shows whether the deal has a foto or not.
 - **metadata**, shows the metadata of the deal, see: [deal metadata](parts/deal-metadata.md)
 - **start**, shows the starting time of the deal, see: [deal start](parts/start-or-end.md)
 - **end**, shows the ending time fo the deal, see: [deal end](parts/start-or-end.md)
 - **spot**, shows information about the spot where the deal is, see: [deal spot](parts/spot.md)

EXAMPLES:
---------

 - **lat & lng**, [http://api.feest.je/1/deal/get/?lat=52.092323&lng=4.276106](http://api.feest.je/1/deal/get/?lat=52.092323&lng=4.276106)
 - **sort**,
 - **deal**, [http://api.feest.je/1/deal/get/?deal=1a21704e654b5825931f5ea3d0d08d08](http://api.feest.je/1/deal/get/?deal=1a21704e654b5825931f5ea3d0d08d08)
 - **highlighted**, [http://api.feest.je/1/deal/get/?highlighted=true](http://api.feest.je/1/deal/get/?highlighted=true)
 - **spot**, [http://api.feest.je/1/deal/get/?spot=e1b3311da9ed6421ad334aa3425d9c31](http://api.feest.je/1/deal/get/?spot=e1b3311da9ed6421ad334aa3425d9c31)