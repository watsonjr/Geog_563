## Satellite Dataset Overview in GEE
### Dataset Name
### Search this dataset:
`Landsat-8 Collection 2 Tier 1 TOA Reflectance

### Provider
<Agency or program>  
(Examples: NASA, USGS, ESA/Copernicus, NOAA)

### Description
Short description of the dataset including:
- Sensor or mission name
- Primary purpose (surface reflectance, radar, thermal, etc.)
- Processing level (TOA, SR, L2A, etc.)

Example:  
This dataset contains Level-2 surface reflectance imagery from Landsat 8 OLI/TIRS with atmospheric correction and cloud QA bands.

---

## Spectral Bands
Lists all the bands within the dataset and includes description of each variable:
- Band name
- Description
- Wavelength/Frequency
- Resolution

---

## Additional Metadata

| Property | Description |
|---------|-------------|
| Temporal Coverage | <Start–End years> |
| Temporal Resolution | <Revisit period> |
| Spatial Resolution | <Meters> |
| Orbit Type | <Sun-synchronous, polar, geostationary, etc.> |
| Cloud Masking | <QA bands description> |
| Units | <Reflectance, radiance, dB, Kelvin, etc.> |
| Projection | <Default projection info> |

---

## Example GEE Code Snippet to view “print” band list

Copy and paste into GEE code editor: 

// Define geometry
var geometry = ee.Geometry.Point([-121.1, 45.0]);

// Load dataset
var dataset = ee.ImageCollection("LANDSAT/LC08/C02/T1_TOA")
  .filterBounds(geometry);

// Test size
print("Image count:", dataset.size());

// Inspect metadata safely
var first = dataset.first();
print("First image:", first);
print("Band names:", first.bandNames());
## check console to view bands under “band names”



## Reference
https://developers.google.com/earth-engine/datasets


## Best Practices in GEE

### Do not mix client and sever functions in your script.

* Server objects start with ee such as ee.Image and ee.Reducer and any methods on these objects are server functions. Anything else is a client function which can come from Code Editor or JavaScript 

### Do not convert to lists if it is not necessary,

* Only use collection elements (“List”, “Array”) if you need random elements, otherwise use filters on the collection to access individual elements

* In other words use filtering > type conversion to access an element in a collection 

### Try to avoid using ee.Algorithms.If() and reproject()

* This can be memory intensive 

### Use filter() and select() before map() fro better selection

### Use updateMask() instead of mask() 

* mask() avoids the argument whereas updateMask() does a logical of the argument 

### Combine reducers if you need multiple statistics for efficiency 

### Use Export to avoid memory limit issues and time outs 

* Also avoid clip() as this will often lend to increased computation time
* If needed, use clipToCollection() instead, use this instead of featureCollection.geometry() as well

### Use appropriate scales when using reduceToVectors()
* Don’t use this with reduceRegions()

### For neighborhood operation use fastDistanceTransfrom()
* alternatively use reduceNeighborhood() 

### Only sample the amount of data needed 
* can increase cost without increased results 

## References 
https://developers.google.com/earth-engine/guides/best_practices


