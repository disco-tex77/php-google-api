PHP Google API
===

Version 0.1.0

...for Google Map API v3, PHP >= 5, Yii 1.*

###Configuration
---
in your app and/or console configuration file, add these

    'components' => array(
    	'googleMapApi'   => array(
    			'class'             => 'vendor.quexer69.php-google-api.GoogleMapApi',
                /**
                 * Google Maps Image and Geocode API settings
                 */
                'staticmap_api_key' => 'AIzaSyBLBPqma_9xReVGyq22Z0nIYrbymkdqjjo',
                'geocode_api_key'   => 'AIzaSyC5TEafNG5sTT42j4X5RVXxdXnhk5o4Bz8',
                'map_type'          => 'terrain',
                'map_size'          => '520x350',
                'map_sensor'        => false,
                'map_zoom'          => 9,
                'map_scale'         => 1,
                'map_image_path'    => '/images/google_map',
                'language'          => 'de',
    	),
		...
	),


###Usage
---

**Just type in an address string as you do on google maps!**

    $address 	  = '70180 Stuttgart, Germany';

    $filePath     = Yii::app()->googleMapApi->createImage($address,null);

**For query by latitude and longitude**

    $latlng 	  = '48.7632145,9.174027';

    $filePath     = Yii::app()->googleMapApi->createImage(null, $latlng);


###Method descriptions
---

TBD.