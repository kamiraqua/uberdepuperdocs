URL:
----
[http://api.feest.je/1/dm/get](http://api.feest.je/1/dm/get)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)


AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call returns an array filled with direct messages for a user. Depending on the parameters.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - **to**(*string*), returns only direct messages that were send to the given user.(*userid*)
 - **from**(*string*, returns only direct messages that were received from the given user.(*userid*)
 - **with**(*string*), returns only direct messages that were send to or received from the given user.(*userid) 
 - **since**(*timestamp*), returns only direct messages since the given date and time.
 - **until**(*timestamp*), returns only direct messages until the given date and time.

**Extra:**

 - None
 
RESPONSE FIELDS:
----------------

 - **_id**, shows the id of the direct message.
 - **time**, shows the time at which the message was send(*timestamp*)
 - **message**, shows the actual message of the direct message.
 - **from**, shows information about the user who send the message, see:[dm from](parts/dm-user.md)
 - **to**, shows information about the user who received the message, see:[dm to](parts/dm-user.md)
 



EXAMPLES:
---------

 - **to**, [http://api.feest.je/1/dm/get/?to=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/dm/get/?to=9dae1fdbeace59c2008d388d6d3cf242)
 - **from**, [http://api.feest.je/1/dm/get/?from=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/dm/get/?from=9dae1fdbeace59c2008d388d6d3cf242)
 - **with**, [http://api.feest.je/1/dm/get/?with=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/dm/get/?with=9dae1fdbeace59c2008d388d6d3cf242)
 - **since**, [http://api.feest.je/1/dm/get/?since=1300359794](http://api.feest.je/1/dm/get/?since=1300359794)
 - **until**, [http://api.feest.je/1/dm/get/?until=1300359794](http://api.feest.je/1/dm/get/?until=1300359794)
