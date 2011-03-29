URL:
----
[http://api.feest.je/1/relation/destroy/](http://api.feest.je/1/relation/destroy/)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](parts/authentication.md)

SUMMARY:
--------
This call destroys a relation between the logged in user and the given user.

PARAMETERS:
-----------

**Required:**

 - **user**(*string*), the id of the user with who the relation has to be destroyed.
 - **type**(*string*), if follower, makes the given user id unfollow the logged in user, if following, makes the logged in user unfollow the given user.

**Optional:**

 - None

**Extra:**

 - None
 
RESPONSE FIELDS:
----------------

*if it worked, relation-destroy will only return one single field saying true.*

EXAMPLES:
---------
- **user & type**, [http://api.dagje.in/1/relation/destroy/](http://api.dagje.in/1/relation/destroy/) with post data "user=9dae1fdbeace59c2008d388d6d3cf242&type=following"