URL:
----
[http://api.feest.je/1/user/get](http://api.feest.je/1/user/get)

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
This call returns information about users, or just a single user.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - **user**(*string*), returns a user with the given username or userid.
 - **q**(*string*), returns a user with a name similar to the searchvalue.

**Extra:**

 - **basic**(*bool*), if true, returns only the basic information of a user, returns everything otherwise.

RESPONSE FIELDS:
----------------

 - **_id**, shows the id of the user.
 - **name**, shows the name of the user.
 - **username**, shows the username of the user.

*The following fields will only be shown if the user is public*

 - **public**, shows whether the user is public or not.(*bool*)
 - **bio**, shows the biografy of the user.
 - **city**, shows the homecity of the user.
 - **site**, shows the website of the user.
 - **following**, shows an array of people that the user follows, see:[user following](parts/user-follow.md)
 - **stats**, shows the stats of the user, see:[user stats](parts/user-stats.md)
 - **followers**, shows an array of people that follow the user, see:[user followers](parts/user-follow.md)
 - **checkins**, shows the last checkin of the user, see:[user checkins](parts/user-checkin.md)
 - **kingdom**, shows the kingdom of the user, see:[user kingdom](parts/user-kingdom.md)
 - **medals**, shows the medals that the user earned, see:[user medals](parts/user-medals.md)
 - **spots**, shows the spots that the user visited, see:[user spots](parts/user-spots.md)

EXAMPLES:
---------

 - **user**, [http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242)
 - **q**, [http://api.feest.je/1/user/get/?q=sinterklaas](http://api.feest.je/1/user/get/?q=sinterklaas)
 
 - **basic**, [http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242&basic=true](http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242&basic=true)