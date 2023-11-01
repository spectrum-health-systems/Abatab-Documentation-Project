> Last updated: **November 1, 2023**

<div align="center">

![](_attachments/AbatabDocumentationProjectLogo.png)
	<h1>
		File headers
	</h1>
</div>

***

# File headers

All `.cs` files should have a file header comment.

All file headers have a maximum width of 80 characters, with the exception of URLs that are longer than 80 characters.

## Primary header

Abatab.asmx.cs is the main entry point for Abatab, so it contains the primary header for Abatab:

```csharp
// =============================================================================
// Abatab: A custom web service/framework for myAvatar.
// https://github.com/spectrum-health-systems/Abatab
// Copyright (c) A Pretty Cool Program. All rights reserved.
// Licensed under the Apache 2.0 license.
//
// For details about this release, please see the local Source Code README.md:
//   Abatab/README.md
// =============================================================================
```

## Class header

Each class has a simple header:

```csharp
// -----------------------------------------------------------------------------
// Namespace.ClassName.cs: Description of class.
// https://spectrum-health-systems.github.io/Abatab-Documentation-Project/<FileName.html>
// bYYMMDD.HHMM
// -----------------------------------------------------------------------------
```

Example:

```csharp
// -----------------------------------------------------------------------------
// Abatab.Abatab.asmx.cs: Entry point for Abatab.
// https://spectrum-health-systems.github.io/Abatab-Documentation-Project/Source%20code/Abatab/Abatab.asmx.cs.html
// b231030.1043
// -----------------------------------------------------------------------------
```
