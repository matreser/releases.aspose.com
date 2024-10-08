---
date: "2024-07-20"
id: "aspose-barcode-for-net-24-8-release-notes"
slug: "aspose-barcode-for-net-24-8-release-notes"
linktitle: "Aspose.BarCode for .NET 24.8 Release Notes"
title: "Aspose.BarCode for .NET 24.8 Release Notes"
author: "Alexander Gavriluk"
weight: 104
description: "A summary of recent changes, enhancements and bug fixes in Aspose.BarCode for .NET 24.8.0 (August 2024) release."
type: "repository"
layout: "release"
hideChildren: false
toc: false
family_listing_page_title: "Aspose.BarCode for .NET 24.8 Release Notes"
keywords:
- "2024"
- "August"
- "new"
- "release"
- "changelog"
menuItemWithNoContent: false
---

{{% alert color="primary" %}}

This article contains release notes information for [**Aspose.BarCode for .NET 24.8 (August 2024)**](https://releases.aspose.com/barcode/net/new-releases/aspose.barcode-for-.net-24.8/).

{{% /alert %}}
## **All Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|BARCODENET-38022|AustralianPostShortBarHeight is ignored|Bug + Enhancement + Reopened|
|BARCODENET-38369|Update PZN encoder, decoder|Enhancement|
|BARCODENET-39081|Add tests for functionality that was added in release 24.6 including setters and getters|Quality issue|
|BARCODENET-39089|Recognize and add QrVersion to QRExtendedParameters in BarCodeResult|Enhancement|
|BARCODENET-39102|Fix issue with failed meterеd tests|Quality issue|

## Public API changes and backwards compatibility

### AustraliaPost, Planet, Postnet barcodes generation

AustraliaPost, Planet, Postnet barcodes generation is changed.

***AustralianPost.AustralianPostShortBarHeight*** by default is set to zero and calculated by default as 0.26 from ***BarHeight***.
```cs
//AustraliaPost barcode generation
BarcodeGenerator gen = new BarcodeGenerator(EncodeTypes.AustraliaPost, "6212345678AP");
gen.Parameters.Barcode.AustralianPost.AustralianPostEncodingTable = CustomerInformationInterpretingType.CTable;
gen.Parameters.Barcode.BarHeight.Pixels = 100;

// If short bar is not specified, it is scaled to 0.26 * BarHeight
gen.Parameters.Barcode.AustralianPost.AustralianPostShortBarHeight.Pixels = 10;
gen.Parameters.Barcode.Padding.Left.Pixels = 10;
gen.Parameters.Barcode.Padding.Top.Pixels = 10;
gen.Parameters.Barcode.Padding.Right.Pixels = 10;
gen.Parameters.Barcode.Padding.Bottom.Pixels = 10;
gen.Save("AustraliaPost.png", BarCodeImageFormat.Png);
```

***Postal.PostalShortBarHeight*** by default is set to zero and calculated by default as 0.5 from ***BarHeight***.
```cs
//Planet, Postnet barcodes generation
BarcodeGenerator gen = new BarcodeGenerator(EncodeTypes.Postnet, "5552357000");
gen.Parameters.Barcode.BarHeight.Pixels = 100;

// If short bar is not specified, it is scaled to 0.5 * BarHeight
gen.Parameters.Barcode.Postal.PostalShortBarHeight.Pixels = 40;

gen.Parameters.Barcode.CodeTextParameters.Location = CodeLocation.None;
gen.Parameters.Barcode.Padding.Left.Pixels = 10;
gen.Parameters.Barcode.Padding.Top.Pixels = 10;
gen.Parameters.Barcode.Padding.Right.Pixels = 10;
gen.Parameters.Barcode.Padding.Bottom.Pixels = 10;
```

### PZN7 and PZN8 barcodes generation

PZN8 and PZN7 encoding and decoding are supported:
- To encode PZN7 it is needed to provide 6 digits or less to CodeText, like "123456".
- To encode PZN8 it is needed to provide 7 digits or more to CodeText, like "1234567".
- Provided last checksum digit is ignored and generated by the barcode engine.

```cs
//encode and decode PZN7
using (BarcodeGenerator gen = new BarcodeGenerator(EncodeTypes.PZN, "123456"))
using (BarCodeReader reader = new BarCodeReader(gen.GenerateBarCodeImage(), DecodeType.PZN))
    foreach (BarCodeResult result in reader.ReadBarCodes())
        Console.WriteLine(result.CodeTypeName + ":" + result.CodeText);

//encode and decode PZN8
using (BarcodeGenerator gen = new BarcodeGenerator(EncodeTypes.PZN, "1234567"))
using (BarCodeReader reader = new BarCodeReader(gen.GenerateBarCodeImage(), DecodeType.PZN))
    foreach (BarCodeResult result in reader.ReadBarCodes())
        Console.WriteLine(result.CodeTypeName + ":" + result.CodeText);
```

### QR, MicroQR, RectMicroQR barcodes recognition

QR, MicroQR, RectMicroQR barcodes recognition parameters obtained new public properties ***QRVersion***, ***MicroQRVersion***, ***RectMicroQRVersion*** and ***QRErrorLevel***, which have been added to the ***QRExtendedParameters***.

```cs
using (BarcodeGenerator gen = new BarcodeGenerator(EncodeTypes.QR, "Aspose"))
{
    gen.Parameters.Barcode.QR.QrVersion = QRVersion.Version15;
    gen.Parameters.Barcode.QR.QrErrorLevel= QRErrorLevel.LevelM;
    using (BarCodeReader reader = new BarCodeReader(gen.GenerateBarCodeImage(), DecodeType.QR))
    {
        reader.ReadBarCodes();
        Console.WriteLine("Codetext: {0}", reader.FoundBarCodes[0].CodeText);
        Console.WriteLine("QR version: {0}", reader.FoundBarCodes[0].Extended.QR.QRVersion);
        Console.WriteLine("Error level: {0}", reader.FoundBarCodes[0].Extended.QR.QRErrorLevel);
    }
}
```

Result:
```txt
Codetext: Aspose
QR version: Version15
Error level: LevelM
```