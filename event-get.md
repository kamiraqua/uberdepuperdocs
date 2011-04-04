URL:
----
[http://api.feest.je/1/event/get](http://api.feest.je/1/event/get)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
False, see: [authentication](parts/authentication.md)

SUMMARY:
--------
This call returns events. Depending on the parameters.


PARAMETERS:
-----------

**Required:**
 
 - None

**Optional:**

 - **lat**(*float*), returns events within [radius] meters from the given latitude. Requires lng.
 - **lng**(*float*), returns events within [radius] meters from the given longitude. Requires lat.
 - **since**(*timestamp*), returns events since the given date and time.
 - **until**(*timestamp*), returns events until the given date and time.
 - **when**(*string*),
 - **event**(*string*), returns only the event with the given eventid.
 - **name**(*string*), returns events with the given event name.
 - **q**(*string*), returns events with a name similar to the given value.
 - **spot**(*string*), returns all events at the given spot.
 - **user**(*string*), returns all events that the given user(*userid or username*) attended to.


**Extra:**

 - **radius**(*int*), returns all events in the given radius of a spot or geolocation. Radius in km. Default is 5 km.
 - **sort**(*string*), if start, sorts events by the starting time, if end, sorts events by the ending time, if popular, sorts events by the number of people attending, if undefined, does nothing.  
 - **who**(*string*), if set to friends, returns events that were created by your friends.
 - **hasphoto**(*bool*), if true, returns only events with photos, returns all events otherwise. 
 - **limit**(*int*), sets the number of events that should be returned. Defaulted to 25.
 - **skip**(*int*), sets the number of events that should be skipped. Defaulted to 0.
 - **when**(*string*), if 'calendar', returns all events that the user signed op to, if 'now', returns all events that are happening right now, if 'upcoming', returns all events that are starting in the future, if 'allways', returns all events. Defaulted to 'allways'.

RESPONSE FIELDS:
----------------
 -	**_id**, the id of the event.
 -	**name**, the name of the event.
 -	**nameslug**, the nameslug of the event.
 -	**type**,  the type of the event.
 -	**location**, the geolocation of the event, see:[event location](parts/location.md)
 -	**start**, the start time of the event, see:[event start](parts/start-or-end.md)
 -	**end**, the end time of the event, see:[event end](parts/start-or-end.md)
 -	**spot**, Information about the spot where the event is at, see:[event spot](parts/spot.md)
 -	**user**, information about the user who created the event, see:[event user](parts/user.md)
 -	**stats**, the stats of the event, see:[event stats](parts/event-stats.md)



EXAMPLES:
---------
 -	**lat & lng**, [http://api.feest.je/1/event/get/?lat=52.3861821&lng=4.8715395](http://api.feest.je/1/event/get/?lat=52.3861821&lng=4.8715395)
 -	**since**, [http://api.feest.je/1/event/get/?since=1278187200](http://api.feest.je/1/event/get/?since=1278187200)
 -	**until**, [http://api.feest.je/1/event/get/?until=1278187200](http://api.feest.je/1/event/get/?until=1278187200)
 -	**when**, 
 -	**event**, [http://api.feest.je/1/event/get/?event=113421c0d5bf160a82755f501eb17fe8](http://api.feest.je/1/event/get/?event=113421c0d5bf160a82755f501eb17fe8)
 -	**name**, [http://api.feest.je/1/event/get/?name=the%20next%20web%20conference%202011](http://api.feest.je/1/event/get/?name=the%20next%20web%20conference%202011)
 -	**q**, [http://api.feest.je/1/event/get/?q=the%20next%20web%20conference%202011](http://api.feest.je/1/event/get/?q=the%20next%20web%20conference%202011)
 -	**spot**, [http://api.feest.je/1/event/get/?spot=607582b687a1d3af4981e6467301ec20](http://api.feest.je/1/event/get/?spot=607582b687a1d3af4981e6467301ec20)
 -	**user**, [http://api.feest.je/1/event/get/?user=sinterklaas](http://api.feest.je/1/event/get/?user=sinterklaas)

 -	**radius**, [http://api.feest.je/1/event/get/?spot=607582b687a1d3af4981e6467301ec20&radius=100](http://api.feest.je/1/event/get/?spot=607582b687a1d3af4981e6467301ec20&radius=100)
 -	**sort**,
 -	**who**,
 -	**hasphoto**, [http://api.feest.je/1/event/get/?lat=52.3861821&lng=4.8715395&hasphoto=true](http://api.feest.je/1/event/get/?lat=52.3861821&lng=4.8715395&hasphoto=true)
