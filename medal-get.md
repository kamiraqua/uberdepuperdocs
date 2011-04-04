URL:
----
[http://api.feest.je/1/medal/get](http://api.feest.je/1/medal/get)

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
This call returns an array filled with all the available medals.

PARAMETERS:
-----------

**Required:**

 - None
 
**Optional:**

 - **user**(*string*), returns the medals that were earned by the given user(*userid*)
 - **medal**(*string*), returns only the medal with the given medalid.
 - **earned**(*bool*), if true, returns only medals that were earned by the user, if false, returns only medals that were not earned by the user. Requires user.
 - **limit**(*int*), sets the number of medals that should be returned. Defaulted to 25.
 - **skip**(*int*), sets the number of medals that should be skipped. Defaulted to 0.

**Extra:**

 - None

RESPONSE FIELDS:
----------------

 - **_id**, shows the id of the medal.
 - **name**, shows the name of the medal.
 - **slug**, shows the nameslug of the medal.
 - **points**, shows the points that are earned with earning this medal.
 - **user**, shows information whether an user earned the medal, see:[medal user](parts/medal-user.md)
 

EXAMPLES:
---------

 - **user**, [http://api.feest.je/1/medal/get/?user=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/medal/get/?user=9dae1fdbeace59c2008d388d6d3cf242)
 - **medal**, [http://api.feest.je/1/medal/get/?medal=36e9041569cd540a2441ca6809f16b14](http://api.feest.je/1/medal/get/?medal=36e9041569cd540a2441ca6809f16b14)
 - **earned**, [http://api.feest.je/1/medal/get/?user=9dae1fdbeace59c2008d388d6d3cf242&earned=true](http://api.feest.je/1/medal/get/?user=9dae1fdbeace59c2008d388d6d3cf242&earned=true)