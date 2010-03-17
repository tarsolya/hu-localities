# HU LOCALITIES

YAML formatted database containing all locality - city, town, village, etc. - names from Hungary, geotagged with precision, imported from geonames.org.

## Features

* Each record is geotagged (lat, long) with precision support.
* Zip code for each record
* County and region names
* Source database included

## Using

Record structure is following:

    :city => Name of locality
    :latitude => Latitude of locality
    :longitude => Longitude of locality
    :precision => Geocode precision (from 1 (estimated) to 6 (centroid))
    :county => Full name of the locality's county
    :county_code => ISO code for the locality's county
    :zip => ZIP code for the locality

You can import the YAML file easily:

    yml = YAML.load_file 'hu.geonames.org.yml'
    
Then you can iterate:

    yml.each_key { |key| puts yml[key][:city], yml[key][:zip] }

## Other

Visit http://geonames.org for more good stuff on everything geo.

