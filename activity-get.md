URL:
----
[http://api.feest.je/1/activity/get](http://api.feest.je/1/activity/get)

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
This call returns activities from the activity stream. Depending on the parameters.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - **user**(*string*), returns activities of the given user(*username or userid*). This includes earning medals, becoming king and check-ins.
 - **spot**(*string*), returns activities at the given spot(*spotid*).
 - **medal**(*string*), returns activities that earned the given medal(*medalid*).
 - **event**(*string*), returns activity at the given event(*eventid*).
 - **lat**(*float*), returns activities at the given geolocation. Requires lng.
 - **lng**(*float*), returns activities at the given geolocation. Requires lat.
 - **activity**(*string*), returns only the activity with the given activityid.
 - **type**(*string*), returns only activities of a certain type(checkin, etc) 
 - **hasphoto**(*bool*), if true, returns activities with photos, returns all activities otherwise.

**Extra:**

 - **since**(*timestamp*), returns activities since the given date and time.
 - **until**(*timestamp*), returns activities until the given date and time.
 - **limit**(*int*), sets the number of activities that should be returned. Is defaulted to 25.
 - **skip**(*int*), sets the numer of activities that should be skipped. Is defaulted to 0.
 - **radius**(*int*), sets the range in which to return activities. Range in kilometers. Is defaulted to 1.

RESPONSE FIELDS:
----------------

 -	**_id**, the id of the activity.
 -	**type**, the type of the activity. Can be checkin, king, medal, event_created or event_checkin.

 *If the activity type is "checkin" the following fields will be returned.* 

 -	**message**, shows the message that was put at the moment of checking in.
 -	**points**, shows the points that were earned with this checkin.
 -	**time**, shows the time of the check in(*timestamp*).
 -	**stats**,  shows the stats of the check in, see: [activity stats](parts/activity-stats.md)
 -	**user**, shows information about the user who checked in, see: [activity user](parts/activity-user.md)
 -	**spot**, shows information about the spot where the check in was, see: [activity spot](parts/activity-spot.md)

 *If the activity type is "king" the following fields will be returned.*

 -	**points**, shows the points that were earned by becoming king.
 -	**time**, shows the time that the user became king(*timestamp*).
 -	**user**, shows information about the user who became king, see: [activity king](parts/activity-user.md)
 -	**spot**, shows information about the spot where the user became king, see: [activity spot](parts/activity-spot.md)
 -	**stats**, shows the stats about the becoming of king, see: [activity stats](parts/activity-stats.md) 

 *If the activity type is "medal" the following fields will be returned.*

 -	**points**, shows the points that were earned by earning the medal.
 -	**time**, shows the time at which the medal was earned(*timestamp*).
 -	**user**, shows information about the user who earned the medal, see: [activity user](parts/activity-user.md)
 -	**medal**, shows information about the medal that was earned, see: [activity medal](parts/activity-medal.md)
 -	**stats**, shows the stats of the earning of the medal, see: [activity stats](parts/activity-stats.md)

 *If the activity type is "event_created" the following fields will be returned.*

 -	**points**, shows the points that were earned by creating the event.
 -	**time**, shows the time at which the event was created(*timestamp*).
 -	**user**, shows information about the user who created the event, see: [activity user](parts/activity-user.md)
 -	**event**, shows information about the event that was created, see: [activity event](parts/activity-event.md)
 -	**spot**, shows information about the spot where the event is located, see: [activity spot](parts/activity-spot.md)
 -	**stats**, shows the stats of the creation of the event, see: [activity stats](parts/activity-stats.md) 

 *If the activity type is "event_checkin" the following fields will be returned.*

 -	**message**, shows the message that was put at the moment of checking in.
 -	**points**, shows the points that were earned with this check in.
 -	**time**, shows the time of the check in(*timestamp*)
 -	**stats**, shows the stats of the check in, see: [activity stats](parts/activity-stats.md)
 -	**user**, shows information about the user who checked in, see: [activity user](parts/activity-user.md)
 -	**event**, shows information about the even where the user checked in, see: [activity event](parts/activity-event.md)
 -	**spot**, shows information about the spot where the user checked in, see: [activity spot](parts/activity-spot.md)


EXAMPLES:
---------
 - **user**, [http://api.feest.je/1/activity/get/?user=sinterklaas](http://api.feest.je/1/activity/get/?user=sinterklaas)
 - **spot**, [http://api.feest.je/1/activity/get/?spot=607582b687a1d3af4981e6467301ec20](http://api.feest.je/1/activity/get/?spot=607582b687a1d3af4981e6467301ec20)
 - **medal**, [http://api.feest.je/1/activity/get/?medal=dc157bce80c16939c676b4e81fe318b6](http://api.feest.je/1/activity/get/?medal=dc157bce80c16939c676b4e81fe318b6)
 - **event**, [http://api.feest.je/1/activity/get/?event=113421c0d5bf160a82755f501eb17fe8](http://api.feest.je/1/activity/get/?event=113421c0d5bf160a82755f501eb17fe8)
 - **lat & lng**, [http://api.feest.je/1/activity/get?lat=53.2159195&lng=6.5616468](http://api.feest.je/1/activity/get?lat=53.2159195&lng=6.5616468)
 - **activity**, [http://api.feest.je/1/activity/get?activity=c19ff03f75fa27948e8e15c04aa4e28c](http://api.feest.je/1/activity/get?activity=c19ff03f75fa27948e8e15c04aa4e28c)
 - **type**, [http://api.feest.je/1/activity/get?type=checkin](http://api.feest.je/1/activity/get?type=checkin)
 - **hasphoto**, [http://api.feest.je/1/activity/get?hasphoto=true](http://api.feest.je/1/activity/get?hasphoto=true)

 - **since**, [http://api.feest.je/1/activity/get/?user=sinterklaas&since=1290261031](http://api.feest.je/1/activity/get/?user=sinterklaas&since=1290261031)
 - **until**, [http://api.feest.je/1/activity/get/?user=sinterklaas&until=1290261031](http://api.feest.je/1/activity/get/?user=sinterklaas&until=1290261031)