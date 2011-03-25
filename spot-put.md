URL:
----
[http://api.feest.je/1/spot/put/](http://api.feest.je/1/spot/put/)

REQUEST METHOD:
---------------
POST (Content-Type: application/json)

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
 - **address**(*array*), the address of the spot.
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

 - **name**, the name of the spot.
 - **address**, information about the address of the spot, see: [spot addess](<link naar address pag>)
 - **create_date**, shows the exact date and time at which the spot was created(*timestamp*)
 - **creator**, shows the id of the user that created the spot.
 - **nameslug**, shows the nameslug of the spot.
 - **location**, shows the geolocation of the spot, see: [spot location](<link naar location>)
 - **_id**, shows the id of the spot.

EXAMPLES:
---------

- **general**, [http://api.feest.je/1/spot/put/](http://api.feest.je/1/spot/put/) with post data "{"name":"testspot","address":{"city":"Groningen"}}"