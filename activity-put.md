URL:
----
[http://api.feest.je/1/activity/put](http://api.feest.je/1/activity/put)

REQUEST METHOD:
---------------
POST(content-type: application/x-www-form-urlencoded)


RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call adds an activity to the activity stream.

PARAMETERS:
-----------

**Required:**

 - **id**(*string*), sets the id of of the event or spot of the activity.
 - **type**(*string*), sets the type of the activity. Can be 'checkin' or 'event_checkin'.

**Optional:**

 - **message**(*string*), adds a message to the activity. The maximum length of the message is 100 characters.
 - **push**(*bool*), if true, it pushes the activity to followers, does nothing otherwise.
 - **social**(*string*), sets to which social media the activity should be pushed. Can be twitter, facebook, foursquare and hyves. All media are separated by an ':'.
 
 
**Extra:**

 - None

RESPONSE FIELDS:
----------------
 - **_id**, shows the id of the newly created activity.
 - **type**, shows the type of the newly created activity.
 - **points**, shows the points that were earned with this activity.
 - **stats**, shows the stats of the newly created activity, see:[activity stats](parts/activity-stats.md)
 - **user**, shows information about the user who commited the activity, see:[activity user](parts/activity-user.md)
 - **spot**, shows information about the spot where the user commited the activity, see:[activity spot](parts/activity-spot.md)
 

EXAMPLES:
---------
 
 - **id & type**, [http//api.feest.je/1/activity/put/](http//api.feest.je/1/activity/put/) with post data "id=607582b687a1d3af4981e6467301ec20&type=checkin"
 This call checks the user in at the spot with the id '607582b687a1d3af4981e6467301ec20'.
 
 - **message**, [http//api.feest.je/1/activity/put/](http//api.feest.je/1/activity/put/) with post data "id=607582b687a1d3af4981e6467301ec20&type=checkin&message=awesome%20checkin"
 This call checks the user in at the spot with the id '607582b687a1d3af4981e6467301ec20' and adds the message 'awesome checkin'.
 
 - **push**, [http//api.feest.je/1/activity/put/](http//api.feest.je/1/activity/put/) with post data "id=607582b687a1d3af4981e6467301ec20&type=checkin&push=true"
 This call checks the user in at the spot with the id '607582b687a1d3af4981e6467301ec20' and pushes that message to all of his followers.
 
 - **social**, [http//api.feest.je/1/activity/put/](http//api.feest.je/1/activity/put/) with post data "id=607582b687a1d3af4981e6467301ec20&type=checkin&social=twitter"
 This call checks the user in at the spot with the id '607582b687a1d3af4981e6467301ec20' and pushes that message to twitter.