URL:
----
[http://api.feest.je/1/relation/create/](http://api.feest.je/1/relation/create/)

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
This call creates a relation between the logged in user and the given user.

PARAMETERS:
-----------

**Required:**
 
 - **user**(*string*), the id of the user to create the relation with.
 - **json**(*string*), fill with a number of userid's to create a relation with multiple users. Constructed like this: ["userid", "userid"]

**Optional:**

 - None
 
**Extra:**

 - None

RESPONSE FIELDS:
----------------
*for every user that a relation was made with, the following fields will be returned*

 - **_id**, the id of the user that the relation was made with.
 - **name**, the name of the user that the relation was made with.
 - **username**, the username of the user that the relation was made with.

 
 *It might happend that the reply is just '[]' this means that the logged in user already follows the users you tried to create a relation with.* 

EXAMPLES:
---------

- **user**, [http://api.feest.je/1/relation/create/](http://api.feest.je/1/relation/create/) with post data "user=9dae1fdbeace59c2008d388d6d3cf242"
This call creates a relation between the logged in user and the user with the id '9dae1fdbeace59c2008d388d6d3cf242'.
- **json**, [http://api.feest.je/1/relation/create/](http://api.feest.je/1/relation/create/) with post data "json=["b88ac32d37c9741ca0a682152b6f48c5", "9dae1fdbeace59c2008d388d6d3cf242"]"
This call creates a relation between the logged in user and the two users with id 'b88ac32d37c9741ca0a682152b6f48c5' and '9dae1fdbeace59c2008d388d6d3cf242'