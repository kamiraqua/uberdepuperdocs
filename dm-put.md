URL:
----
[http://api.feest.je/1/dm/put/](http://api.feest.je/1/dm/put/)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authenticaton](<link naar auth pagina>)

SUMMARY:
--------
This call sends a direct message to the given user.

PARAMETERS:
-----------

**Required:**

 - **message**(*string*), the actual message.
 - **user**(*string*), the id of the user to send the message to.

**Optional:**

 - None
 
**Extra:**

 - None

RESPONSE FIELDS:
----------------

 - **_id**, the id of the direct message.

EXAMPLES:
---------

- **message & user**, [http://api.dagje.in/1/dm/put/](http://api.dagje.in/1/dm/put/) with post data "message=this is a direct message&user=9dae1fdbeace59c2008d388d6d3cf242"