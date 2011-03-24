URL:
----
[http://api.feest.je/1/event/rsvp/](http://api.feest.je/1/event/rsvp/)

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
 - **event**, contains an array containing the id of the event, see: [rsvp event](<link naar event>)
 - **user**, contains an array containing the id of the user, see: [rsvp user](<link naar user pagina>)
 - **start**, contains an array containing the starting time of the event, see: [rsvp start](<link naar start pagina>)
 - **end**, contains an array containing the ending time of the event, see: [rsvp end](<link naar end pagina>)
 - **status**, the status of the user regarding the event.
 
EXAMPLES:
---------
- **event**, [http://api.feest.je/1/event/rsvp/](http://api.feest.je/1/event/rsvp/) with post data "event=113421c0d5bf160a82755f501eb17fe8"
This call signs the user up for the event with id '113421c0d5bf160a82755f501eb17fe8'