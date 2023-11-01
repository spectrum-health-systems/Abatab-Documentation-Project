> Last updated: **November 1, 2023**

<div align="center">
<table>  
  <tr>

![](_attachments/AbatabDocumentationProjectLogo.png)

  </tr>
  <tr>
Development Guidelines: Comments
  </tr>
</table>
</div>

***

# File headers

All `.cs` files should have a file header comment.

All file headers have a maximum width of 80 characters, with the exception of URLs that are longer than 80 characters.

## Primary header

Abatab.asmx.cs is the main entry point for Abatab, so it contains the primary header for Abatab:

```
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

```
// -----------------------------------------------------------------------------
// Namespace.ClassName.cs: Description of class.
// https://spectrum-health-systems.github.io/Abatab-Documentation-Project/<FileName.html>
// bYYMMDD.HHMM
// -----------------------------------------------------------------------------
```

Example:

```
// -----------------------------------------------------------------------------
// Abatab.Abatab.asmx.cs: Entry point for Abatab.
// https://spectrum-health-systems.github.io/Abatab-Documentation-Project/Source%20code/Abatab/Abatab.asmx.cs.html
// b231030.1043
// -----------------------------------------------------------------------------
```


# XML documentation

Abatab XML documentation comments follow [Microsoft's recommendations](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/xmldoc/recommended-tags).

XML documentation
- XML documentation comments should be included in the source code, and not in external files.
- All publicly visible types and their public members should be documented.
- It is recommended that private members also be documented.
- Documentation text should be written using complete sentences ending with full stops.

## Formatting

### Text formatting

XML documentation comments can using the following formatting tags:

- `<b>bold</b>`
- `<i>italic</i>`
- `<u>underline</u>`

### Greater than/Lesser than

To user greater than (">") and lesser than ("<") signs:

- Greater than: `&gt;`
- Lesser than: `&lt;`

### Code blocks

To insert a single line of code, or inline code, `<c>just put the code between these</c>`

To create a code block

```csharp
<code>
Put the code in a code block  
<code>
```

## XML tags

### Summary

The summary should be short, and contained to a single line.

Example:

```csharp
/// <summary>Compares two numbers to determine if they are the same.</summary>
```

### Parameter

Parameter tags should describe each parameter.

Example:

```csharp
/// <param name="numberOne">The first number.</param>
/// <param name="numberTwo">The second number.</param>
```

### Remarks

Remarks are optional, and should give additional, important information.

Remarks should be split into paragraphs using the `<para></para>` tags.

Remarks can contain lists:

```csharp
/// <remarks>
///     <para>
///         This method needs two things:
///         <list type="number">
///             <item>A number</item>
///             <item>Another number</item>
///         </list>
///     </para>
///     <para>
///         Numbers to be compared <u>must</u>:
///         <list type="bullet">
///             <item>
///                 Be &gt;= zero
///             </item>
///             <item>
///                 Be <i>less</i> than <c>100</c>
///             </item>
///             <item>
///                 Not be an <b>even</b> number
///             </item>
///         </list>
///     </para>
/// </remarks>
```

Remarks can contain tables, but they kind of look wonky in Visual Studio (but look good in DocFX):

```csharp
/// <remarks>
///     <para>
///         Keep in mind:
///         <list type="table">
///             <listheader>
///                 <term>Number</term>
///                 <description>Validity</description>
///             </listheader>
///             <item>
///                 <term>1</term>
///                 <description>Valid.</description>
///             </item>
///             <item>
///                 <term>2</term>
///                 <description>Invalid</description>
///             </item>
///             <item>
///                 <term>200</term>
///                 <description>Invalid</description>
///             </item>
///         </list>
///     </para>
/// </remarks>
```

### Example

Example comments don't show in Visual Studio (?), but look fine in DocFX.

An example of...uh...an example XML comment:

```csharp
        /// <example>
        ///     Here is an example of the code:
        ///     <code>
        ///     if(numberOne == numberTwo)
        ///     {
        ///         return true;
        ///     }
        ///     else
        ///     {
        ///         return false;
        ///     }
        ///     </code>
        /// </example>
```

### Return

The return content should be short, and contained to a single line.

Example:

```csharp
/// <returns>A boolean value.</returns>
```

### Value

Example:

```csharp
/// <value>Default value is <c>false</c></value>
```

### Put it all together

This example of an XML documentation comment details the correct tag order:

```csharp
/// <summary>Compares two numbers to determine if they are the same.</summary>
/// <param name="numberOne">The first number.</param>
/// <param name="numberTwo">The second number.</param>
/// <remarks>
///     <para>
///         This method needs two things:
///         <list type="number">
///             <item>A number</item>
///             <item>Another number</item>
///         </list>
///     </para>
///     <para>
///         Numbers to be compared <u>must</u>:
///         <list type="bullet">
///             <item>
///                 Be &gt;= zero
///             </item>
///             <item>
///                 Be <i>less</i> than <c>100</c>
///             </item>
///             <item>
///                 Not be an <b>even</b> number
///             </item>
///         </list>
///     </para>
///     <para>
///         Keep in mind:
///         <list type="table">
///             <listheader>
///                 <term>Number</term>
///                 <description>Validity</description>
///             </listheader>
///             <item>
///                 <term>1</term>
///                 <description>Valid.</description>
///             </item>
///             <item>
///                 <term>2</term>
///                 <description>Invalid</description>
///             </item>
///             <item>
///                 <term>200</term>
///                 <description>Invalid</description>
///             </item>
///         </list>
///     </para>
///     <para>
///         For more information please review the <see href="../link/GoesHere.html#Anchor">Abatab Documentation Project</see>.
///     </para>
/// </remarks>
/// <example>
///     Here is an example of the code:
///     <code>
///     if(numberOne == numberTwo)
///     {
///         return true;
///     }
///     else
///     {
///         return false;
///     }
///     </code>
/// </example>
/// <returns>A boolean of true or false.</returns>
/// <value>Default value is <c>false</c></value>

```
