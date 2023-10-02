# Radiometric-correction
Apply relative radiometric correction to satellite images in order to improve the quality of the image and remove non-uniformities.

**Introduction**
Performing a relative radiometric correction using lab and real satellite data.

**Objectives**
Create a solution that can apply relative radiometric correction to satellite images in order to improve the quality of the image and remove non-uniformities.

- Using the dark and flat field calibration data write code that can create a relative radiometric correction.
- Apply the correction to the lab and real linescan images taking into account the metadata, with the output stored GeoTIFF file.
- Solution should be automated and be able to correct different linescan images based on input parameters.
- Create metrics to show how the quality of the image has changed after applying the correction.

**Solution**
This automated approach allows usera to apply a relative radiometric correction to a target image using a dark field, and flatfield calibration image

This approach has several steps, which are dealt with by a series of functions, including:

- Import the data
- Correct the image with calibration data
- Perform data analysis to assess correction
- Present the data and analysis

**Performannce analysis**

_Check quality of lab based correction_
Check how the variance has changed in the reference (lab) based image using the satandard deveiation, with a lower standdarad deviation (while maintaining the same mean) the target. This will be demonstrated with a narrower peak (lower variance) about the mean in the histogram.

_Check spatial consistency of corrected image with variagram_
Perform spatial variagram to to ensure that the same spatial characteristics (structure) are preserved before and after correction, using a random selection of points within the image.

Three variograms are presented, before, after and the difference, each using the same coordinates

Comapre the variagrams between the target and corrected images, which should show some change, but only limited. Too large a change sugests the fundemental surface reflectance has been erroneously altered.
