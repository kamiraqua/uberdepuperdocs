URL:
----
[http://api.feest.je/1/event/photo/](http://api.feest.je/1/event/photo/)

REQUEST METHOD:
---------------
POST

RATE LIMIT:
-----------
True, see: [rate limiting](parts/rate-limiting.md)

AUTHENTICATION REQUIRED:
------------------------
False, see: [authentication](<link naar authenticationpagina>)

SUMMARY:
--------
This call adds a photo to an existing event.

PARAMETERS:
-----------

**Required:**

 - **event**(*string*), the id of the event that should get the photo.

**Optional:**

 - **basephoto**(*string*), a base64 string decoded image.

**Extra:**

 - None

RESPONSE FIELDS:
----------------

 - **small**, shows a string with the url to the small sized photo link.
 - **medium**, shows a string with the url to the medium sized photo link.
 - **large**, shows a string with the url to the large sized photo link.
 - **extralarge**, shows a string with the url to the extra-large sized photo link.

EXAMPLES:
---------
 - **general**, [http://api.feest.je/1/event/photo/](http://api.feest.je/1/event/photo/) with post data     {"event":"4fd4ba3e38b91d0ba10160c1769eb804","basephoto":"iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAIAAACQkWg2AAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAb5JREFUeNpi/P//PwMpgAmraFJGIRBhlWJEtuHZ8xfTZi3cd/DI589fgFxeXh4ne5ustHgpSQksGjZu2dHZNxWo9L+oLMPPbyAhdi7G14+B2sqLsv19PFA03Lh1JzQ6FaTCP5NBRp3h6jGQpLYVw5Ob/zdOB+pfvXS2hpoKwg9dfVOBJFtECZu8BhszI5ueNQgBGUBuRAlcARCwQJx++uwFVl3rTCeDCFV+oMiEi2+AZIG+CJBccVt42jnr02ePApUBPcME8ShQQl1cIEVL8MW3P0AEVApEEDZQECgFVABUBlTM9PTZC6B3gXzO90+B5O7HX+59+sXDygREQAaQC5cCKgMqZgB6+tSZ8zomDp6Nc7/8+vsfDC69+QFEEDZQECgFVABUBuSC/GBqbAAMuxeHt2daezhKcwFF9j8FBSucDZQCKgAqQ4RSTETw7w9v7q+auevxVyD6/e8/EEHYQEGgFFABesQB4wEYGzxKmmI2nq+PbAeKiNp4vjqy/cu968AYAMYDugZgHE+fvXDx8jVoiSc2MiQzNR7oJCxpCRInew8cWbJ8LcidkcHODjbICQmLBni6ApLw9IMMAAIMAHma/94S7t7gAAAAAElFTkSuQmCC"}



