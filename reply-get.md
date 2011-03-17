URL:
----
[http://api.feest.je/1/reply/get](http://api.feest.je/1/reply/get)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
False, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call returns an array filled with replies. Depending on the parameters.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - **event**(*string*), returns replies on the given event.(*eventid*)
 - **spot**(*string*), returns replies on the given spot.(*spotid*)
 - **activity**(*string*), returns replies on the given activity.(*activityid*)
 - **q**(*string*), returns replies with a message similar to the searchvalue.

**Extra:**

 - None

RESPONSE FIELDS:
----------------

 - **_id**, shows the reply id.
 - **message**, shows the actual message of the reply.
 - **time**, shows the time at which the reply was created.
 - **type**, shows the type of the reply. This can be 'event','spot' or 'activity'.
 - **user**, shows information about the user who placed the reply, see:[reply user](<link naar user pagina>)
 
EXAMPLES:
---------
 - **event**, [http://api.feest.je/1/reply/get/?event=113421c0d5bf160a82755f501eb17fe8](http://api.feest.je/1/reply/get/?event=113421c0d5bf160a82755f501eb17fe8)
 - **spot**, [http://api.feest.je/1/reply/get/?spot=607582b687a1d3af4981e6467301ec20](http://api.feest.je/1/reply/get/?spot=607582b687a1d3af4981e6467301ec20)
 - **activity**, [http://api.feest.je/1/reply/get/?activity=e73255376b51135cb3ce726421cff6ce](http://api.feest.je/1/reply/get/?activity=e73255376b51135cb3ce726421cff6ce)
 - **q**, [http://api.feest.je/1/reply/get/?q=hey](http://api.feest.je/1/reply/get/?q=hey)