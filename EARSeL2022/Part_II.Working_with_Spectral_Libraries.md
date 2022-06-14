# Part II: Working with Spectral Libraries

Aim of this session is to learn how to use Spectral Libraries in the EnMAP-Box


## How to create a Spectral Library Window

1. Open the EnMAP-Box
2. Open an EnMAP image / any other raster image
3. Activate the "Identify map tool" and it's "Spectral Profile" option 
4. Click on a raster image pixel to collect a spectral profile and show it in a new spectral library window.


## Collect profiles from raster images



## Spectral Libraries are vector layers


## Create a 2nd empty Spectral Library Window


Let's add profiles to the 2nd library.


## The Spectral Profile Source Panel




## The EnMAP-Box Spectral Library Model

A spectral library is a QGIS vector layer that contains one or more fields that store spectral profiles.
A spectral profile field is a field of 
    (i) type binary (BLOB) or text (VARCHAR, unlimited) that is designated to a 
    (ii) Spectral Profile editor widget

=> your vector layer can contain other BLOB field, e.g. to store picture

A single spectral profile is a JSON object with an array "y" that contains n > 0 spectral profile values:

````json
{
    "y": [34, 23, 45, 63, ... , 45]
}
````

In addition, the JSON object can described the "y" values by their position on an "x" axis (e.g. the wavelength), 
unit name of the "y" and "x" values and (for convenience with the ENVI format), bad band values:

---|--------
y | y values, a vector with n spectral values
x | x values, a vector with n wavelength values
xUnit | unit of x values, e.g. 'nm' or 'Nanometer'
yUnit | unit of y values, e.g. 'Reflectance' or 'Radiance'
bbl | bad band list, i.e. a vector with n bad-band multipliers. E.g. 0 for bad/masked and 1 for good/not masked
----|-------

| member | content                                                                                    |
|--------|--------------------------------------------------------------------------------------------|
| y      | an array with n profile values                                                             |
| x      | an array with n profile value locations, e.g. the band wavelengths                         |
| yUnit  | string that describes the unit of y values, e.g. "Reflectance"                             |
| xUnit  | string that describes the x value unit, e.g. "nm" or "Nanometers"                          |
| bbl    | a "bad band list", i.e. a vector with n bad-band multipliers. 0 = masked, > 0 = not masked |


Other metadata to describe spectra profiles are stored in additional vector layer fields.

## 1. Spectral Libraries are Vector Layers



## 2 how to make a vector layer a Spectral Library



## 3. Import Spectral Profiles measured in field


## 4. Save the spectral library 