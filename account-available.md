URL:
----
[http://api.feest.je/1/account/available/](http://api.feest.je/1/account/available/)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
False, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call returns whether an username is available or not.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - **username**(*string*), returns whether the given username is available

**Extra:**

 - None

RESPONSE FIELDS:
----------------

 - **available**, if true, the given username is available, if false, the given username is not available.


EXAMPLES:
---------
 - **username**, [http://api.feest.je/1/account/available/?username=sinterklaas](http://api.feest.je/1/account/available/?username=sinterklaas)