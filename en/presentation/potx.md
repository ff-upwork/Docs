{
  "date" : "2019-10-11",
  "keywords" : [ "potx file", "potx file format", "what is a potx file", "file", "potx example", "potx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "POTX - Microsoft PowerPoint Presentation Template",
  "description":"Learn about POTX file format and APIs that can create and open POTX files.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a POTX file?

Files with .POTX extension represent Microsoft PowerPoint template presentations that are created with Microsoft PowerPoint 2007 and above. This format was created to replace the [POT](/presentation/pot/) file format that is based on the binary file format and is supported with PowerPoint 97-2003. The files generated can be used to create presentations that have same layout and other settings required to be applied to new files. These settings can include styles, backgrounds, colour palette, fonts and defaults. Such files are generated in order to create ready-to-use template files for official use.

## Brief History ##

It was in the early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents, of different types, under this new Standard were identified by appending "X" in their extensions, where "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, less changes of corruption and well formatted images representation.

## File Format Specifications ##

Files generated with office Open XML file format is a collection of XML files along with other files that provide links between all the constituent files. This collection is actually a compressed archive that can be extracted to view its contents. To do so, just rename the POTX file extension with zip and extract it for observing its contents.

Following sections shed some light on each one of these.

### [Content_Types].xml ###

This is the only file that is found at the base level when the zip is extracted. It lists the content types for parts within the package. All references to the XML files included in the package are referenced in this XML file. Following is a content type for a slide part:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
If new parts need to be added to the package, it can be done by adding the new part and update any relationships within the .rels files. It has to be kept in mind that for such a change, the Content_Types.xml must also be updated.

### \_rels (Folder) ###

Relationships between the other parts and resources outside of the package are maintained by the relationships part. The Relationships folder contains a single XML file that stores the package-level relationships. Links to the key parts of the PPTX files are contained in this file as URIs. These URIs identify the type of relationship of each key part to the package. This includes the relationship to primary office document located as ppt/presentation.xml and other parts within docProps as core and extended properties.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Each part of document that is the source of one or more relationships will have its own relationships part where each such relationship part is found within a \_rels sub-folder of the part and is named by appending '.rels' to the name of the part. The main content part (presentation.xml) has its own relationships part (presentation.xml.rels). It contains relationships to other other parts of the content such as slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, as well as the URIs for external links.

#### Explicit Relationship ####

For an explicit relationship, a resource is referenced using the Id attribute of a <Relationship> element. That is, the Id in the source maps directly to an Id of a relationship item, with an explicit reference to the target.

For example, a slide might contain a hyperlink such as this:
```
<a:hlinkClick r:id#"rId2">
```
The r:id#"rId2" references the following relationship within the relationships part for the slide (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Implicit Relationship ####

For an implicit relationship, there is no such direct reference to a `<Relationship> Id`. Instead, the reference is understood.

### ppt Folder ###

This is the main folder that contains all the details about the contents of the Presentation. By default, it has following folders:

* \_rels
* theme
* slides
* slideLayouts
* slideMasters

and following xml files:

* presentation.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## References ##

* [[MS-PPTX] - PPTX File Format](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)
