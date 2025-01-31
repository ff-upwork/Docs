{
  "date" : "2019-10-11",
  "keywords" : [ "obj file", "obj file format", "what is an obj file", "file", "obj example", "obj file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OBJ File Format",
  "description":"Learn about OBJ file format and APIs that can open and create OBJ files.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an OBJ File?

**OBJ** files are used by Wavefront's Advanced Visualizer application to define and store the geometric objects. Backward and forward transmission of geometric data is made possible through OBJ files. Both polygonal geometry like points, lines, texture vertices, faces and free-form geometry (curves and surfaces) are supported by OBJ format.  This format does not support animation or information related to light and position of scenes.

An OBJ file is usually an end product of the 3D modeling process generated by a CAD (Computer Aided Design). The default order to store vertices is counter-clockwise avoiding explicit declaration of face normals. Though OBJ files declare scale information in a comment line yet no units have been declared for OBJ coordinates.

## History of 3D OBJ Format

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. The file format is open and has been implemented by other vendors for their 3D graphics application. Wavefront Technologies kept this file format open source and neutral.

## OBJ File Format

In 3D objects, encoding the surface geometry is a challenging job that OBJ file format accomplished very well. This format is quite versatile as it offers a number of choices to encode surface geometry. Following are three allowed formats having their own benefits and shortcomings:

### Tessellation with Polygonal Faces

The OBJ file format facilitates the user to tessellate a 3D model surface using simple or complex geometric shapes. For surface geometry encoding of a model, a file stores the vertices and normal to each polygon. Though tessellation increases coarseness to the model, yet It is necessary to discover the correct balance between size of a file and in its print quality.

### Free-form Curve

OBJ file format allows the user-defined free-form surface curves to specify the surface geometry of a model. As free-form curves are more complex than polygonal faces since, with few mathematical parameters, curved lines can be best defined by freeform curves. Therefore, with fewer data as compared to polygonal tessellations, free-form curves used to generate a high-quality encoding of any 3D model without expanding the file size.

### Free-form Surfaces

OBJ file format also specifies the tiling of surface geometry with free-form surface patches. This kind of freeform surface patches (NURBS) is very suitable for surfaces without rigid radial dimensions like the body of a truck, the wings of helicopter or the hull of a boat. Use of freeform surfaces are very advantageous as they are more precise to keep file sizes smaller at higher precision. These surfaces are essential part of aerospace and automotive industry where the low precision is unforgiving.

The following keywords are arranged by data type to define surface geometry.


|Elements|Free-form curve/surface body statements|Free-form curve/surface attributes
---|---|---|
|p|Point|parm|Parameter values|deg|Degree
|l|Line|trim|Outer trimming loop|bmat|Basis matrix
|f|Face|hole|Inner trimming loop|step|Step size
|curv|Curve|scrv|Special curve|cstype|Curve or surface type
|curv2|2D curve|sp|Special point|**Connectivity and Grouping of surfaces**
|surf|Surface|end|End statement|con|connect
|**Display/render attributes**|g|Group name
|bevel|Bevel interpolation|shadow_obj|Shadow casting|s|Smoothing group
|lod|Level of detail|trace_obj|Ray tracing|mg|Merging group
|d_interp|Dissolve interpolation|ctech|Curve approximation technique|o|Object name
|c_interp|Color interpolation|stech|Surface approximation technique|
|usemtl|Material name|mtllib|Material library|
|**Geometric vertices**|
|v|Geometric vertices|vn|Vertex normals|
|vt|Texture vertices|vp|Parameter space vertices|

### Color and Texture

OBJ file allows color and texture information to store in an associated file format called the Material Template Library (MTL). Multi-color geometric models render using these two files together. MTL files are ASCII based and facilitates in computer rendering by describing light reflecting properties of a surface using the model of Phong reflection. The standard has been adopted by a large number of software vendors who take its advantage for interchange of materials. MTL format is slightly outdated for not having support in latest technologies such as specular and parallax maps.

## References

* [Wavefront .obj file](https://en.wikipedia.org/wiki/Wavefront_.obj_file)
