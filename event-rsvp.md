URL:
----
[http://api.feest.je/1/event/rsvp/](http://api.feest.je/1/event/rsvp/)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](parts/authentication.md)

SUMMARY:
--------
This call sets the user to a state of attending to the given event.

PARAMETERS:
-----------

**Required:**

 - **event**(*string*), the id of the event that the user wants to sign up to.

**Optional:**

 - None

**Extra:**

 - None
 
RESPONSE FIELDS:
----------------

 - **_id**, shows the id of the event that you just signed up to.
 - **event**, contains an array containing the id of the event, see: [rsvp event](parts/event.md)
 - **user**, contains an array containing the id of the user, see: [rsvp user](parts/user.md)
 - **start**, contains an array containing the starting time of the event, see: [rsvp start](parts/start-or-end.md)
 - **end**, contains an array containing the ending time of the event, see: [rsvp end](parts/start-or-end.md)
 - **status**, the status of the user regarding the event.
 
EXAMPLES:
---------
- **event**, [http://api.feest.je/1/event/rsvp/](http://api.feest.je/1/event/rsvp/) with post data "event=113421c0d5bf160a82755f501eb17fe8"
This call signs the user up for the event with id '113421c0d5bf160a82755f501eb17fe8'