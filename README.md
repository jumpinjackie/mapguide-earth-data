# MapGuide NaturalEarth Dataset

This repository contains the resources for the MapGuide NaturalEarth dataset.

These resources use the [NaturalEarth dataset](http://naturalearthdata.com) for vector and raster data

# Installation

[Download](https://naturalearth.s3.amazonaws.com/10m_cultural/10m_cultural.zip) and extract the NaturalEarth 10m_cultural dataset

[Download](https://naturalearth.s3.amazonaws.com/10m_raster/NE1_LR_LC_SR_W_DR.zip) and extract the NaturalEarth 10m raster with Shaded Relief, Water, and Drainages

Assuming the following directory layout on Windows

```
C:\MapGuideEarth
   - 10m_cultural
      - [extracted contents of 10m_cultural.zip]
   - 10m_raster
      - [extracted contents of NE1_LR_LC_SR_W_DR.zip]
```

Set up an unmanaged data alias `NaturalEarthData` that points to `C:\MapGuideEarth`

Once done, you can create the package file to load by doing the following:

 1. Git clone this repo
 2. Enter this clone directory and create a zip file containing the following files/directories: 
    * `Library`
    * `MgResourcePackageManifest.xml`
 3. Rename the zip file so that it has a `.mgp` extension
 4. Load this package into MapGuide via the Site Administrator or MapGuide Maestro

Load this package file using the MapGuide Site Administrator or MapGuide Maestro.

# Updating the resources in this package (for contributors)

If you want contribute to this dataset, you will need to do the following.

 1. Git clone this repo
 2. Enter this clone directory and create a new feature branch
 3. Create a zip file containing the following files/directories: 
    * `Library`
    * `MgResourcePackageManifest.xml`
 4. Rename the `.zip` file so it has a `.mgp` extension
 5. Load this package into MapGuide (via the Site Administrator or MapGuide Maestro)
 6. Use MapGuide Maestro to add/edit/rename/delete changes.
 7. Once you have finished making and testing your resource changes, use MapGuide Maestro to create a package of `Library://NaturalEarth/` and all resources within it
 8. Unzip the contents of your created package back into your git clone
 9. Git commit and push your changes
 10. Open a new pull request