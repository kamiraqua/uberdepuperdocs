URL:
----
[http://api.feest.je/1/users/suggest](http://api.feest.je/1/users/suggest)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
True, see:[authentication](parts/authentication.md)

SUMMARY:
--------
This call returns a row of users that are suggested to follow.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - None
 
**Extra:**

 - **limit**(*int*), sets the number of users that should be returned. Defaulted to 25.
 - **skip**(*int*), sets the number of users that should be skipped. Defaulted to 0.
 - **random**(*string*), sets whether the suggestions should be random or not. Can be 'true' or 'false'. Defaulted to false.

RESPONSE FIELDS:
----------------

 - **_id**, shows the userid of the suggested user.
 - **name**, shows the name of the suggested user.
 - **username**, shows the username of the suggested user.
 - **public**, if this row exists, it says whether the user is public or not. If this row does not exist, the user is NOT public.
 - **sex**, shows the sex of the user. Only visible if defined.
 - **type**, shows the base on which the suggestion was made.
 - **matches**, shows the number of matches with friends.

EXAMPLES:
---------
 - **general**, [http://api.feest.je/1/users/suggest](http://api.feest.je/1/users/suggest)