URL:
----
[http://api.feest.je/1/user/timeline/](http://api.feest.je/1/user/timeline/)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authentication pagina>)

SUMMARY:
--------
This call returns the timeline for the logged in user.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - **type**(*string*), returns only the given type of activity. Can be 'checkin', 'event_checkin', 'event_rsvp', 'medal', 'king', ...
 - **since**(*timestamp*), returns only activities since the given date and time.
 - **until**(*timestamp*), returns only activities until the given date and time.
 - **show**(*string*), if friends, returns only activities from user that follow you and follow you back, returns all otherwise. 
 - **medal**(*string*), returns only activities in which the given medal was earned.
 - **spot**(*string*), returns only activities at the given spot.
 - **event**(*string*), returns only activities at the given event.
 - **lat**(*float*), returns only activities at the given geolocaton. Requires lng.
 - **lng**(*float*), returns only activities at the given geolocation. Requires lat.
 
**Extra:**


RESPONSE FIELDS:
----------------
 - **_id**, shows the id of the activity.
 - **type**, shows the type of the activity.
 - **message**, shows the message that was put with the activity.
 - **points**, shows the points that were earned with the activity.
 - **time**, shows the time of the activity.(*timestamp*)
 - **stats**, shows the stats of the activity, see: [activity stats](parts/timeline-stats.md)
 - **user**, shows the basic information of the user who commited the activity, see: [activity user](parts/user.md)
 - **spot**, shows information about the spot where the activity took place, see: [activity spot](parts/spot.md)

EXAMPLES:
---------
 - **type**, [http://api.feest.je/1/user/timeline/?type=checkin](http://api.feest.je/1/user/timeline/?type=checkin)
 - **since**, [http://api.feest.je/1/user/timeline/?since=1300790306](http://api.feest.je/1/user/timeline/?since=1300790306)
 - **until**, [http://api.feest.je/1/user/timeline/?until=1300790306](http://api.feest.je/1/user/timeline/?until=1300790306)
 - **show**, [http://api.feest.je/1/user/timeline/?show=friends](http://api.feest.je/1/user/timeline/?show=friends)
 - **medal**, [http://api.feest.je/1/user/timeline/?medal=aea9e04cb8f1a644770821055bdd8fe5](http://api.feest.je/1/user/timeline/?medal=aea9e04cb8f1a644770821055bdd8fe5)
 - **spot**, [http://api.feest.je/1/user/timeline/?spot=607582b687a1d3af4981e6467301ec20](http://api.feest.je/1/user/timeline/?spot=607582b687a1d3af4981e6467301ec20)
 - **event**, [http://api.feest.je/1/user/timeline/?event=113421c0d5bf160a82755f501eb17fe8](http://api.feest.je/1/user/timeline/?event=113421c0d5bf160a82755f501eb17fe8)
 - **lat & lng**, [http://api.feest.je/1/user/timeline/?lat=53.2159195&lng=6.5616468](http://api.feest.je/1/user/timeline/?lat=53.2159195&lng=6.5616468)