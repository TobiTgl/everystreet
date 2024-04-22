# Everystreet [Fork](https://github.com/matejker/everystreet)
see [www.everystreetchallenge.com](http://www.everystreetchallenge.com)
 
Modified some files so it works for me (Usage instructions from original repo didn't work on my machine)

Things I am using for it:
-  Pycharm 2024.1
- Python 3.9

How I made it work:
- Changes in [requirements.txt](https://github.com/TobiTgl/everystreet/commit/41e5ad3d1c661be9c7514ac07e502a06c341a574) and  [two imports](https://github.com/TobiTgl/everystreet/commit/598f63bda133a1289a229ac637cc451146ebcef6)
- Let Pycharm handle the rest  😂 
- added notebooks that create gpx files and png of route if needed and saves them in ./gpx ./images
- use [https://gpx.studio/](https://gpx.studio/) to fine tune gpx route

# Notebooks
## from_place.ipynb (creates the route for the city based on the name)
Only location name needs to be changed

## polygon.ipynb (creates route only for selected polygon)
1. open [www.everystreetchallenge.com](http://www.everystreetchallenge.com) 
2. open developer settings 
3. select polygon on map
4. send request
5. copy opject from first request payload
6. create json file with coordinates (needs to be geojson slightly different that payload)
    - konstanznew.json = polygons from everystreetchallenge.com
    - konstanzpolygon.json = geojson file that is used by notebook
7. Change polygon file in notebook
