URL:
----
[http://api.feest.je/1/account/settings](http://api.feest.je/1/account/settings)

REQUEST METHOD:
---------------
GET

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

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
 - **email**, shows informaton about when to give an email notification to the user, see: [account email](parts/account-email.md)
 - **notify**, shows information about when to give a push notification to the user, see: [account notify](parts/account-notify.md)
 - **public**, shows whether the account is public or not.
 - **social**, shows information about what other social networks the user uses, see: [account social](parts/account-social.md)
 - **connection**, shows information about to what social networks the account is connected, see: [account connection](parts/account-connection.md)


EXAMPLES:
---------
 - **general**, [http://api.feest.je/1/account/settings/](http://api.feest.je/1/account/settings/)