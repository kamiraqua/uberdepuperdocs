URL:
----
[http://api.feest.je/1/event/update/](http://api.feest.je/1/event/update/)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authenticaton pagina>)

SUMMARY:
--------
This call updates the given event to the newly given values.

PARAMETERS:
-----------

**Required:**

 - **event**(*string*), the id of the event that has to be updated.

**Optional:**

 - **name**(*string*), the new name of the event.
 - **spot**(*string*), the id of the new spot where the event will occur.
 - **start**(*array*), expects an array with a single value called 'time'.
	- **time**(*timestamp*), the starting time of the event.
 - **end**(*array*), expects an array with a single value called 'time'.
	- **time**(*timestamp*), the ending time of the event.
 - **location**(*array*), an array filled with the geolocation of the event.
	- **lat**(*float*), the latitude of the geolocation.
	- **lng**(*float*), the longitude of the geolocation.
 - **metadata**(*array*), an array filled with the metadata of the event.
	- **website**(*string*), the url of the website for the event.
	- **description**(*string*), the description for the event.
	- **tags**(*string*), the tags for the event. Tags separated by a ','.
 - **invite**(*array*), an array filled with people who are invited to the event.
	- **users**(*string*), the userid's that are invited to the event. Separated by a ','.
	- **external**(*string*), an json object containing an array of objects. The json objects are constructed like this: '[{"email":"info@email.com","name":"Personal Name"}]'
	
 **Extra:**
  
 - None

RESPONSE FIELDS:
----------------

EXAMPLES:
---------