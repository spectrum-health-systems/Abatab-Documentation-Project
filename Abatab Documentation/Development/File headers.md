<!-- 
	Last updated: 231030
	This documentation is incomplete.
-->

<div align="center">

![](_attachments/AbatabDocumentationProjectLogo.png)
	<h1>
		File headers
	</h1>
</div>

***

# File headers

All file headers have a maximum width of 80 characters.

## Primary header

Abatab.asmx.cs is the main entry point for Abatab, so it contains the primary header for Abatab:

```
// =============================================================================
// Abatab: A custom web service/framework for myAvatar.
// https://github.com/spectrum-health-systems/Abatab
// Copyright (c) A Pretty Cool Program. All rights reserved.
// Licensed under the Apache 2.0 license.
// 
// For more information, please see the Abatab Documenation Project
// https://spectrum-health-systems.github.io/Abatab-Documentation-Project/
// =============================================================================
```

### Development branch header

The development branch Abatab.asmx.cs has an additional header:

```
// =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
// This is the development version of Abatab, and is not intended for use in
// production environments.
//
// For production environments, please visit the Abatab Community Release:
// https://github.com/spectrum-health-systems/Abatab-Community-Release
// =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
```

### Community Release header

The Community Release Abatab.asmx.cs has an additional header:

```
// =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
// This is the Abatab Community Release
// 
// For the development version of Abatab, please visit:
// https://github.com/spectrum-health-systems/Abatab
// =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
```

## Class header

Each class has a simple header:

```
// -----------------------------------------------------------------------------
// ClassName.cs
// Description of class.
// bYYMMDD.HHMM
// -----------------------------------------------------------------------------
```

Example:

```
// -----------------------------------------------------------------------------
// Abatab.asmx.cs
// Entry point for Abatab.
// b231030.1043
// -----------------------------------------------------------------------------
```
