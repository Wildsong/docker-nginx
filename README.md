# docker-nginx

This is a test for nginx, it sets up a couple of "client" servers
as a config test.

Note if the proxy is up but the content server is down, then 
you will get "upstream" errors.

Requests for other content should stay in the web-server
that lives in the proxy.


## Test cases

For CC, test these URLs, they are the ones we need to have functional.

This is a flask microservice
https://giscache.co.clatsop.or.us/photos/property/59210
https://giscache.co.clatsop.or.us/photos/tn/property/59210

this is mapproxy
https://giscache.co.clatsop.or.us/ # root for mapproxy
https://giscache.co.clatsop.or.us/osip/demo/?srs=EPSG%3A3857&format=image%2Fjpeg&wms_layer=osip2018

this is static content served directly from nginx
https://giscache.co.clatsop.or.us/photos/static
https://giscache.co.clatsop.or.us/photos/waterway/5114
https://giscache.co.clatsop.or.us/photos/waterway/ph5114.jpg
https://giscache.co.clatsop.or.us/photos/tn/waterway/5114
https://giscache.co.clatsop.or.us/photos/bridges/604A
https://giscache.co.clatsop.or.us/photos/bridges/604A.jpg
https://giscache.co.clatsop.or.us/photos/tn/bridges/604A
https://giscache.co.clatsop.or.us/precincts/Precinct_119.pdf
https://giscache.co.clatsop.or.us/precinct_tn/Precinct_119.png    note there is no S -- "precinct" not "precincts"

this is another nginx instance right now
https://capacity.co.clatsop.or.us/cases

This just redirects to a different server (Matomo)
https://echo.co.clatsop.or.us/

The following simulated URLs should work. Make these work and you should be able to make the above work in deployment.

https://arctic.wildsong.biz/photos/property/59210
https://arctic.wildsong.biz/photos/tn/property/59210
https://arctic.wildsong.biz/ # root for mapproxy
https://arctic.wildsong.biz/osip/demo/?srs=EPSG%3A3857&format=image%2Fjpeg&wms_layer=osip2018
https://arctic.wildsong.biz/photos/waterway/5114
https://arctic.wildsong.biz/photos/waterway/ph5114.jpg
https://arctic.wildsong.biz/photos/tn/waterway/5114
https://arctic.wildsong.biz/photos/bridges/604A
https://arctic.wildsong.biz/photos/bridges/604A.jpg
https://arctic.wildsong.biz/photos/tn/bridges/604A
https://arctic.wildsong.biz/photos/static
https://arctic.wildsong.biz/precincts/Precinct_119.pdf
https://arctic.wildsong.biz/precinct_tn/Precinct_119.png
https://arctic.wildsong.biz/city-aerials

https://maps.wildsong.biz/

