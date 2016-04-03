ShinyGeoip
=====

This API contains the sourcecode of the [saurabhsharma.me/geoip/](http://saurabhsharma.me/geoip/) website. It is an HTTP API to
request location data for IP addresses. Responses can be in JSON or JSONP format.
The API is based on the [Maxmind GeoLite2 Database](http://dev.maxmind.com/geoip/geoip2/geolite2/).

## Demo/Examples
The live version of this API can be found at: [saurabhsharma.me/geoip/](http://saurabhsharma.me/geoip/)
Here you will also find example requests.
 
## Requirements
To run your own instance of ShinyGeoip all you'll need is a webserver that supports PHP and URL rewriting.

## Installation
To setup you own API follow the following steps:

1. Download/Clone this repository to your webserver.
2. Run ```composer install``` to install required dependencies. If composer is not yet installed on your server please
check [getcomposer.org](https://getcomposer.org/).
3. Download a copy of the [GeoLite2 Database](http://dev.maxmind.com/geoip/geoip2/geolite2/) to the ```data``` folder.
If you need to adjust this path you can do so in the ```www/index.php``` file.
4. Point your webserver to the ```www``` folder and rewrite all requests to the index.php file.

You should now have your own instance up and running.

### Optional steps

* Maxmind provides a [PHP extension](http://maxmind.github.io/GeoIP2-php/) which is a drop-in replacement for the
PHP based database reader. Using this extension brings an enormous performance boost and you should use this extension
whenever possible.
* You may want to adjust the homepage template in ```src/Responder/html/home.html.php``` with your own domain
and texts.
