---
id: "aspose-diagram-for-net-21-12-release-notes"
slug: "aspose-diagram-for-net-21-12-release-notes"
linktitle: "Aspose.Diagram for .NET 21.12 Release Notes"
title: "Aspose.Diagram for .NET 21.12 Release Notes"
weight: 1
description: "Aspose.Diagram for .NET 21.12 Release Notes – the latest updates and fixes."
type: "repository"
layout: "release"
---

{{% alert color="primary" %}} 

This page contains release notes information for Aspose.Diagram for .NET 21.12.

{{% /alert %}} 
## **Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMNET-52408|issues when we use the EmfRederSetting EmfPlusPrefer|Enhancement|
|DIAGRAMNET-52438|SaveForegroundPagesOnly for printing|Enhancement|
|DIAGRAMNET-52450|Visio to SVG - Saving raster image separately|Enhancement|
|DIAGRAMNET-51171|Partial rendering of the shapes on saving drawing in PDF format|Bug|
|DIAGRAMNET-51390|Embedded object is not replaced properly|Bug|
|DIAGRAMNET-51800|Visio to SVG - Background Image Missing (PowerPoint is added in the VISIO)|Bug|
|DIAGRAMNET-52423|Page.Copy() doesn't copy Excel Object in diagram|Bug|
|DIAGRAMNET-52443|Missing Shapes while Opening and Saving MS Visio Diagram|Bug|
|DIAGRAMNET-52444|Visio to JPG - Different results generated by the API|Bug|
|DIAGRAMNET-52445|Converting the sample on the Linux and Windows environment have different result|Bug|

## **Public API and Backward Incompatible Changes**
The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.


### **Adds IsSavingImageSeparately in SVGSaveOptions**
- Defines whether Saving Image Separately.

{{< highlight java >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.IsSavingImageSeparately = true;

{{< /highlight >}}


### **Adds CustomImagePath in SVGSaveOptions**
- The user custom path(URL) saved in generated svg file for the image. If not defined by user, Current directory will be used.

{{< highlight java >}}

  o.CustomImagePath = "d:/output/";

{{< /highlight >}}

### **Adds SaveForegroundPagesOnly in PrintSaveOptions**
- Specifies whether all pages will be printed or only foreground.

{{< highlight java >}}

 PrintSaveOptions options = new PrintSaveOptions();
 options.SaveForegroundPagesOnly = true;

{{< /highlight >}}