---
id: "aspose-ocr-for-java-latest-release-notes"
slug: "latest"
weight: 1
date: "2025-02-14"
author: "Vladimir Lapin"
type: "repository"
layout: "release"
title: Latest release
linktitle: "Latest release"
description: A summary of recent changes, enhancements and bug fixes in the latest release of Aspose.OCR for Java.
keywords:
- latest
- patch
- new
- release
- changelog
---

{{% alert color="primary" %}}
This article contains a summary of recent changes, enhancements and bug fixes in **Aspose.OCR for Java 25.2.0 (February 2025)** release.

GPU version: **23.10.1**
{{% /alert %}}

## What was changed

Key | Summary | Category
--- | ------- | --------
OCRJAVA&#8209;411 | Recognition results can now be saved in hOCR format. | New feature

## Public API changes and backwards compatibility

This section lists all public API changes introduced in **Aspose.OCR for Java 25.2.0** that may affect the code of existing applications.

### Added public APIs:

#### `Format.hOcr`

Instructs Aspose.OCR library to save the recognition results in hOCR format - an open standard of data representation for formatted text obtained from OCR. It includes extracted text, style, layout, and other information.

### Updated public APIs:

_No changes._

### Removed public APIs:

_No changes._

## Examples

The code samples below illustrate the changes introduced in this release:

### Save recognition results to hOCR

```java
AsposeOCR api = new AsposeOCR();
// Add an image to OcrInput object
OcrInput input = new OcrInput(InputType.SingleImage);
input.Add("source.png");
// Recognize image
ArrayList<RecognitionResult> results = api.Recognize(input);
// Save result
results[0].Save("result.txt", Format.hOcr);
```
