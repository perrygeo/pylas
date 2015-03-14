# Introduction #

Add your content here.


# Basic steps to convert the shp to a raster DEM with GRASS #
```
      v.in.ogr -o dsn=lidar.shp layer=lidar output=lidar
      g.region vect=lidar
      g.region res=10
      v.surf.rst input=lidar elev=lidar_dem zcolumn=elev
```