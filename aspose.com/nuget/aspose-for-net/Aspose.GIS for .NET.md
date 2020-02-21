This GIS .NET API helps developers render maps, read, write & convert geographic information fetched from vector-based geospatial data formats without needing any other GIS software.

Aspose.GIS for .NET supports working with Shapefile, GeoJSON, ESRI File Geodatabase (FileGDB), Geography Markup Language (GML), Keyhole Markup Language (KML), Scalable Vector Graphics (SVG) and many others.

GIS .NET API allows you to read and write GIS data, convert GIS file formats, and render maps to SVG format. You can also create and analyze feature geometries as well as create basic geometries, such as, Point, MultiPoint, Line, Multiline and Polygon from scratch. The API supports to build non-linear (curve) geometries, linearize non-linear geometries, and control precision mode of calculations.

## GIS API Features
- Render maps to PNG, JPEG, BMP, or SVG.
- Iterate through layer features.
- Read layer features by index.
- Fetch metadata about vector layers.
- Create new layers and datasets as well as work with multi-layer dataset.
- Convert vector data to popular formats.
- Perform re-projection during data conversion.
- Adjust feature attributes while converting.
- Customize styling of each geometry type.
- Perform complex drawing by combining several symbolizers.
- Apply layer rendering rules to control feature visual representation.
- Use value attributes to calculate styling parameters of a feature.
- Perform vector analysis & manipulate geometries.
- Use spatial reference systems.

## Read & Write GIS Formats
**ESRI Shapefile:** SHP, SHX, DBF
**GeoJSON:** JSON, GeoJSON
**TopoJSON:** JSON, TopoJSON
**ESRI File Geodatabase:** GDB
**Google Earth:** KML

## Read GIS Formats
**Geography Markup Language:**  GML
**GPS Exchange Format:** GPX
**MapInfo Interchange Format:** MIF
**MapInfo Tab Format:** TAB, DAT, DBF
**OpenStreetMap:** OSM

## Render GIS Files As Images
**Images:** SVG, PNG, JPEG, JPG, BMP

## Platform Independence
Aspose.GIS for .NET API's uniform model is based on 100% managed code. This API can be used to develop several different types of .NET apps including ASP.NET, WinForms and Windows Services. It is easy to use & deploy, and provides the ideal solution to work with geo-spatial information with .NET Framework 4.7 & .NET Standard 2.0.

## Getting Started with Aspose.GIS for .NET
Are you ready to give Aspose.GIS for .NET a try? Simply execute `Install-Package Aspose.GIS` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.GIS for .NET and want to upgrade the version, please execute `Update-Package Aspose.GIS` to get the latest version.


## Convert a Shapefile to GeoJSON Format with C#
You can execute below code snippet to see how Aspose.GIS API works after adding Aspose.GIS for .NET to your project or check the [GitHub Repository](https://github.com/aspose-gis/Aspose.GIS-for-.NET) for other common usage scenarios. 

```csharp
VectorLayer.Convert(dir + "template.shp", Drivers.Shapefile, dir + "output.json", Drivers.GeoJson);
```

[Product Page](https://products.aspose.com/gis/net) | [Documentation](https://docs.aspose.com/display/gisnet/Home) | [API Reference](https://apireference.aspose.com/net/gis) | [Code Examples](https://github.com/aspose-gis/Aspose.GIS-for-.NET) | [Blog](https://blog.aspose.com/category/gis/) | [Free Support](https://forum.aspose.com/c/gis) |  [Temporary License](https://purchase.aspose.com/temporary-license)