API documentation guide
-----------------------

Every single API call documentation is constructed in the same easy to read manner.
This simple guide will explain to you what everything means.

Every call starts with the **URL**. This is the basic address of the API call.

Just below the URL we have the **REQUEST METHOD**. This should say either GET or POST.
All this field does is tell you the request method of the API call.

Next up is **RATE LIMIT**. This field says whether rate limiting is true or false for
this call. It also contains a link to a page where you can read more specifics about the 
rate limiting.

**AUTHENTICATION REQUIRED** shows you whether there is a form of authentication required to
execute the call. This field also contains a link where you can read more specifics about
the authentication.

The **SUMMARY** gives you a short description of what the call does.

The **PARAMETERS** section lists all the parameters that can be given with this call. The parameters
are split up in 3 sections however. The *Required* sections tells you which parameters are absolutely
needed for the call to work. The *Optional* section lists parameters that are not really necessary
to set. You will always need to set atleast one of them however. The *Extra* parameters are completely
optional. You don't need to set any of those, but you can set all of them if you want.

Every parameter is constructed in the following way:

 - **parameter name**(*parameter type*), some explanation about what the parameter does.
 
Sometimes you will notice that a parameters has more information then listed above. This means that the
parameter does something extra, needs another parameter or might do other things regarding what you set it to.


The **RESPONSE FIELDS** area lists all the fields you get in reply if the call was executed succesfully.
When you notice an area written in the *italics* style, this means that when a special condition is met,
something else will be returned.

Note: all responses are in JSON.

Every response field is constructed in the followig way:

 - **response field name**, an explanation about what the field does.
 
 Sometimes you will notice that a field has more information then listed above. This means there is some
 additional information about that particular field.
 
 The **EXAMPLES** section lists some examples for the call with different parameters. Just so you can see
 what you can acctually do with the feest.je API.