URL:
----
[http://api.feest.je/1/relation/exists](http://api.feest.je/1/relation/exists)

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
This call returns whether a relation exists between 2 users.

PARAMETERS:
-----------

**Required:**

 - **id**(*string*), returns whether this user is linked to another one.(*userid*)
 - **name**(*string*), returns whether this user is linked to the other one.(*userid*)

**Optional:**

 - None

**Extra:**

 - None

RESPONSE FIELDS:
----------------

*If the users are not linked, you will get a single response fields with the value of 'false'*
*If the users are linked however, you will get the following response fields*

 - **notify**, shows whether the user gets notifications from the other user.
 - **mutual**, shows whether the other user follows the user back.


EXAMPLES:
---------
 - **id & name**, [http://api.feest.je/1/relation/exists/?id=bf50ec595844e609cbb346cc144ad737&user=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/relation/exists/?id=bf50ec595844e609cbb346cc144ad737&user=9dae1fdbeace59c2008d388d6d3cf242)