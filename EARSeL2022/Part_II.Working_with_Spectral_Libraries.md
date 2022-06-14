# Part II: Working with Spectral Libraries

Aim of this session is to learn how to use Spectral Libraries in the EnMAP-Box


## How to create a Spectral Library

1. Open the EnMAP-Box
2. Open an EnMAP image / any other raster image
3. Activate the Identify map tool and it's "spectral profile" option 
4. Click on the raster image to collect. This opens a new spectral library window
and add the selected pixel profile to. 


## Create a 2nd empty Spectral Library


Now let's fill this empty spectral library with spectral profiles.


## The EnMAP-Box Spectral Library Model

A spectral library is a QGIS vector layer that contains one or more fields that store spectral profiles.
A spectral profile field is a field of 
    (i) type binary (BLOB) or text (VARCHAR, unlimited) that is designated to a 
    (ii) Spectral Profile editor widget

=> your vector layer can contain other BLOB field, e.g. to store picture

A single spectral profile is a JSON encoded dictionary that contains the following items:


"""python
    {
        y: [34, 23, 45, 63, 45]
    }
"""

In addition, this dictionary may contain further descriptions of the y values, like the wavelength or wavelength unit.

-----------
y | y values, a vector with n spectral values
x | x values, a vector with n wavelength values
xUnit | unit of x values, e.g. 'nm' or 'Nanometer'
yUnit | unit of y values, e.g. 'Reflectance' or 'Radiance'
bbl | bad band list, i.e. a vector with n bad-band multipliers. E.g. 0 for bad/masked and 1 for good/not masked
-----------


## 1. Spectral Libraries are Vector Layers



## 2 how to make a vector layer a Spectral Library



