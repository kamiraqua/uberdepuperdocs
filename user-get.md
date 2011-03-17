URL:
----
[http://api.feest.je/1/user/get](http://api.feest.je/1/user/get)

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
 - **public**, shows whether the user is public or not.(*bool*)
 - **bio**, shows the biografy of the user.
 - **city**, shows the homecity of the user.
 - **site**, shows the website of the user.
 - **following**, shows an array of people that the user follows, see:[user following](<link naar following pagina>)
 - **stats**, shows the stats of the user, see:[user stats](<link naar stats pagina>)
 - **followers**, shows an array of people that follow the user, see:[user followers](<link naar followers pagina>)
 - **checkins**, shows the last checkin of the user, see:[user checkins](<link naar checkin pagina>)
 - **kingdom**, shows the kingdom of the user, see:[user kingdom](<link naar kingdom pagina>)
 - **medals**, shows the medals that the user earned, see:[user medals](<link naar medals pagina>)
 - **spots**, shows the spots that the user visited, see:[user spots](<link naar spots pagina>)

EXAMPLES:
---------

 - **user**, [http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242)
 - **q**, [http://api.feest.je/1/user/get/?q=sinterklaas](http://api.feest.je/1/user/get/?q=sinterklaas)
 
 - **basic**, [http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242&basic=true](http://api.feest.je/1/user/get/?user=9dae1fdbeace59c2008d388d6d3cf242&basic=true)