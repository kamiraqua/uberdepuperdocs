URL:
----
[http://api.feest.je/1/reply/put/](http://api.feest.je/1/reply/put/)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call sets a reply to an activity.

PARAMETERS:
-----------

**Required:**

 - **message**(*string*), the message that the reply must contain.
 - **type**(*string*), the type of the reply.
 - **id**(*string*), the id of the activity to reply to.

**Optional:**

 - **notify**(*bool*), if true, it notifies the other users related to the activity of the reply, does nothing otherwise.

**Extra:**

 - None

RESPONSE FIELDS:
---------------- 
 - **activity**, the id of the activity, see: [reply activity](<link naar activity pagina>)
 - **time**, the time of the reply(*timestamp*).
 - **type**, the type of the reply.
 - **user**, information about the user that placed the reply, see: [reply user](parts/user.md)
 - **message**, the actual message that the reply contained.

EXAMPLES:
---------
 - **message & type & id**, [http://api.feest.je/1/reply/put/](http://api.feest.je/1/reply/put/) with post data "message=this is an reply&type=activity&id=f618bdb9c5320e003b3376512ff6750f"
 - **message & type & id & notify**, [http://api.feest.je/1/reply/put/](http://api.feest.je/1/reply/put/) wiht the post data "message=this is an reply&type=activity&id=f618bdb9c5320e003b3376512ff6750f&notify=true"