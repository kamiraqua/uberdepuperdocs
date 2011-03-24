URL:
----
[http://api.feest.je/1/spot/put/](http://api.feest.je/1/spot/put/)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call creates a spot. 

PARAMETERS:
-----------

**Required:**

 - **name**(*string*), the name of the spot.
 - **adress**(*array*), the address of the spot.
	- **city**(*string*), the city where the spot is at.

**Optional:**

 - **location**(*array*), the geolocation of the spot.
	- **lat**(*float*), the latitude of the geolocation of the spot.
	- **lng**(*float*), the longitude of the geolocation of the spot.
 - **address**(*array*), the address of the spot.
	- **street**(*string*), the street where the spot is at.
	- **zip**(*string*), the zipcode of the spot.
	- **region**(*string*), the region where the spot is at.
	- **country**(*string*), the country that the spot is in.
 - **metadata**(*array*), the metadata of the spot.
	- **website**(*string*), the website of the spot.
	- **description**(*string*), the description of the spot.
	- **tags**(*string*), the tags of the spot. Each tag separated by a ':'.

**Extra:**

 - None

RESPONSE FIELDS:
----------------

EXAMPLES:
---------