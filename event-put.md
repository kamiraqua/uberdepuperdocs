URL:
----
[http://api.feest.je/1/event/put](http://api.feest.je/1/event/put)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authentication pagina>)

SUMMARY:
--------
This call creates an event

PARAMETERS:
-----------

**Required:**

- **name**(*string*), the name of the event.
- **spot**(*string*), the id of the spot where the event will occur.
- **start**(*array*), expects an array with a single value called 'time'.
	- **time**(*timestamp*), the starting time of the event.
- **end**(*array*), expects an array with a single value called 'time'.
	- **time**(*timestamp*), the ending time of the event.
		
**Optional:**

- **social**(*string*), a list of the socials networks to push to. Every network is separated with a ':'.
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

 - **_id**, the id of the event.
 - **name**, the name of the event.
 - **nameslug**, the nameslug of the event.
 - **type**, the type of the event(public, etc)
 - **location**, the geolocation of the event, see: [event location](<link naar location pag>)
 - **start**, the starting time of the event, see:[event start](<link naar start pagina>)
 - **end**, the ending time of the event, see:[event end](<link naar end pagina>)
 - **spot**, information about the spot where the event will take place, see: [event spot](<link naar spot pagina>)
 - **user**, information about the user that created the event, see: [event user](<link naar user pagina>)
 - **stats**, the stats of the the event, see: [event stats](<link naar stats pagina>)

EXAMPLES:
---------

 - **basic event**, [http://api.feest.je/1/event/put](http://api.feest.je/1/event/put) with post data "{"name":"testevent","spot":"607582b687a1d3af4981e6467301ec20","start":{"time":1301047496},"end":{"time":1301048496}} "