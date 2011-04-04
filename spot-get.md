URL:
----
[http://api.feest.je/1/spot/get](http://api.feest.je/1/spot/get)
 
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
This call returns an array of spots. Depending on the parameters. 

PARAMETERS:
-----------
**Required:**

 - None

**Optional:**

 - **Lat**(*float*), returns spots at the given geolocation. *Requires lng*.
 - **Lng**(*float*), returns spots at the given geolocation. *Requires lat*.
 - **Name**(*string*), returns spots with the given name.
 - **City**(*string*), returns spots within the given city.
 - **Street**(*string*), returns spots at the given street.
 - **Q**(*string*), returns spots with a name similar to the value.
 - **Spot**(*string*), returns the spot with the given spotid.
 - **User**(*string*), returns all spots where the given user checked in. (userid)

**Extra:**

 - **Sort**(*string*), if relevancy, sorts spots by similarity to your searchterm (q only), if distance, sorts by distance from your current location, if week, sorts spots by weeks, if month, sorts spots by month, if day, sorts spots by day, if undefined, does nothing.
 - **radius**(*int*), set the range in which to return spots. Range in kilometers. Defaulted to 1.
 - **limit**(*int*), set the number of spots to return. Defaulted to 25.
 - **skip**(*int*), set the number of spots that should be skipped. Defaulted to 0.
 

RESPONSE FIELDS:
----------------
 - **_id**,  shows the id of the spot.
 - **Name**, shows the name of the spot.
 - **Nameslug**, shows the nameslug of the spot.
 - **Location**, shows the geolocation of the spot, see: [location](parts/location.md)
 - **Address**, shows the address of the spot, see: [address](parts/address.md)
 - **Metadata**, shows the metadata of the spot, see: [spot metadata](parts/spot-metadata.md)
 - **Creator**, shows information about the creator of the spot, see: [creator](parts/creator.md)
 - **Stats**, shows the stats of the spot, see: [spot stats](parts/spot-stats.md)
 - **Rating**, shows the rating of the spot, see: [spot rating](parts/rating.md)
 - **King**, shows information about the king of the spot, see: [king](parts/king.md)

EXAMPLES:
---------
 - **lat & lng**, [http://api.feest.je/1/spot/get?lat=53.2159195&lng=6.5616468](http://api.feest.je/1/activity/get?lat=53.2159195&lng=6.5616468)
 - **name**, [http://api.feest.je/1/spot/get?name=Feest.je%20hq](http://api.feest.je/1/spot/get?name=Feest.je%20hq)
 - **city**, [http://api.feest.je/1/spot/get?city=Groningen](http://api.feest.je/1/spot/get?city=Groningen)
 - **street**, [http://api.feest.je/1/spot/get?street=munnekeholm%202](http://api.feest.je/1/spot/get?street=munnekeholm%202)
 - **q**, [http://api.feest.je/1/spot/get?q=feest.je%20hq](http://api.feest.je/1/spot/get?q=feest.je%20hq)
 - **spot**, [http://api.feest.je/1/spot/get?spot=607582b687a1d3af4981e6467301ec20](http://api.feest.je/1/spot/get?spot=607582b687a1d3af4981e6467301ec20)
 - **user**, [http://api.feest.je/1/spot/get/?user=9dae1fdbeace59c2008d388d6d3cf242](http://api.feest.je/1/spot/get/?user=9dae1fdbeace59c2008d388d6d3cf242)
 - **sort**,


