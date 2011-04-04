URL:
----
[http://api.feest.je/1/user/network/](http://api.feest.je/1/user/network/)

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
This call returns all people that are followed by and follow the given user.

PARAMETERS:
-----------

**Required:**

 - **user**(*string*), returns only people that are followed by and/or follow the given user.
 
**Optional:**

 - **show**(*string*), if 'followers', returns only people that follow the given user, if 'following', returns only people that are followed by the user, returns all otherwise.
 - **limit**(*int*), sets the number of users that should be returned. Defaulted to -1.
 - **skip**(*int*), sets the number of users that should be skipped. Defaulted to 0.
 - **showrelation**(*bool*), If true, the relation will be returned, if false, it will not. Defaulted to false.
 - **show**(*string*), 

**Extra:**

 - None

RESPONSE FIELDS:
----------------
 - **_id**, shows the id of the user.
 - **username**, shows the username of the user.
 - **name**, shows the real name of the user.

EXAMPLES:
---------
- **user**, [http://api.feest.je/1/user/network/?user=sinterklaas](http://api.feest.je/1/user/network/?user=sinterklaas)

- **show**, [http://api.feest.je/1/user/network/?user=sinterklaas&show=followers](http://api.feest.je/1/user/network/?user=sinterklaas&show=followers)