Origen de estos datos
---------------------

Son publicados por el gobierno de la provincia de cordoba en 
http://estadistica.cba.gov.ar/Territorio/GeoPortal/tabid/564/language/es-AR/Default.aspx

Projectiones Geograficas
------------------------
Las entidades oficiales utilizan proyecciones **Campo Inchauspe - Gauss-Kruger 
Faja 4** o lo que es equivalente, **EPSG:22194**.
Para obtener informacion sobr estas proyecciones ver u otras
http://spatialreference.org/ref/epsg/22194/
o instalar GDAL (http://www.gdal.org/gdalsrsinfo.html) y usar
```
$ gdalsrsinfo EPSG:22194
```

Para convertir shapefiles en geojson, se utiliza el programa `ogr2ogr`. Por 
ejemplo, para convertir el shapefile `amboy_ejes.shp` a geojson con Latitudes y 
Longitudes, use
```
$ ogr2ogr -f "GEOJSON" amboy-22194.geojson -t_srs EPSG:4326 -s_srs EPSG:22194 amboy_ejes.shp
```

Otras

 - EPGS:22194 Datum campo inchauspe - Gauss-Kruger faja 4

Fuentes de inspiracion para usar estos datos
--------------------------------------------

## Github como API GeoJSON

Ver https://github.com/JasonSanford/gitspatial para usar el repo como API a los 
recursos GeoJSON.

## Visualizacion de GeoJSON online

https://github.com/mapbox/geojson.io