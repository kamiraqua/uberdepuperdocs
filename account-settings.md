URL:
----
[http://api.feest.je/1/account/settings](http://api.feest.je/1/account/settings)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](<link naar ratelimitpagina>)

AUTHENTICATION REQUIRED:
------------------------
True, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call returns the settings of the user that is logged in.

PARAMETERS:
-----------

**Required:**

 - None

**Optional:**

 - None

**Extra:**

 - None

RESPONSE FIELDS:
----------------

*All response fields are bools*

 - **profileimage**, shows whether the user has a profile image or not.
 - **email**, shows informaton about when to give an email notification to the user.[account email](<link naar email pagina>)
 - **notify**, shows information about when to give a push notification to the user. [account notify[(<link naar notify pagina>)
 - **public**, shows whether the account is public or not.
 - **social**, shows information about what other social networks the user uses.[account social[(<link naar account social pagina>)
 - **connection**, shows information about to what social networks the account is connected.[account connection](<link naar connection pagina>)


EXAMPLES:
---------
 - **general**, [http://api.feest.je/1/account/settings/](http://api.feest.je/1/account/settings/)