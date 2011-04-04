URL:
----
[http://api.feest.je/1/event/attending](http://api.feest.je/1/event/attending)

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
This call returns all users that are attending to the given event.

PARAMETERS:
-----------

**Required:**

 - **event**(*string*), returns all users that attend to the given event.(*eventid*)

**Optional:**

 - **checkin**(*bool*), returns only users that acctually checked in at the event.
 - **limit**(*int*), sets the number of users that should be returned. Defaulted to 100.
 - **skip*(*int*), sets the number of users that should be skipped. Defaulted to 0.

**Extra:**

 - None

RESPONSE FIELDS:
----------------

*For every user that attends the following array will be returned*

 - **_id**, shows the id of the attending user.
 - **name**, shows the name of the user.
 - **username**, shows the username of the user.
 - **public**, shows whether the account is public or not.(*bool*)
 - **sex**, shows the sex of the user. If undefined by the user, this row will not be returned.
 - **stats**, shows some stats of the user concerning this event, see: [event attending stats](parts/event-attending-stats.md)


EXAMPLES:
---------
 - **event**, [http://api.feest.je/1/event/attending/?event=113421c0d5bf160a82755f501eb17fe8](http://api.feest.je/1/event/attending/?event=113421c0d5bf160a82755f501eb17fe8)
 
 - **checkin**, [http://api.feest.je/1/event/attending/?event=113421c0d5bf160a82755f501eb17fe8&checkin=true](http://api.feest.je/1/event/attending/?event=113421c0d5bf160a82755f501eb17fe8&checkin=true)