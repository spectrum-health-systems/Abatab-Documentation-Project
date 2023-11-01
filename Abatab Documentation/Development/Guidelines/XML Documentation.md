<div align="center">

![](_attachments/AbatabDocumentationProjectLogo.png)

<h3>
	Development Guidelines: XML Documentation
</h3>
</div>

***

# XML documentation

Abatab uses XML documentation to provide IntelliSense content, as well as API documentation via [DocFX](https://dotnet.github.io/docfx/)

# XML documentation standards

In addition to [Microsoft's XML documentation standards](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/xmldoc/):

- XML documentation comments should be in-line, and not in external files  
- All publicly visible types and their public members should be documented.
- It is recommended that private members also be documented.  
- Documentation text should be written using complete sentences ending with full stops.

# XML documentation formatting

## Text formatting

XML documentation comments can using the following formatting tags:

- `<b>bold</b>`
- `<i>italic</i>`
- `<u>underline</u>`

## Special characters

XML documentation can include the following special characters:

- Greater than: `&gt;`
- Lesser than: `&lt;`
- Space: `&nbsp;`

# XML documentation tags

Abatab XML documentation use [Microsoft's recommended XML tags for C#](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/xmldoc/recommended-tags).

## &lt;summary&gt; tag

The `<summary>` is a short, single line description of what is being documented.

Example:

```csharp
/// <summary>Compares two numbers to determine if they are the same.</summary>
```

## &lt;param&gt; tag

`<param` tags should describe each parameter, and be contained on a single line.

Example:

```csharp
/// <param name="numberOne">The first number.</param>
/// <param name="numberTwo">The second number.</param>
```

### &lt;remarks&gt; tag

`<remarks>` are optional, and should give additional, important information.

Remarks should be enclosed in `<remarks></remarks>` tags, even if they are a single line.

Lengthy remarks should be split into paragraphs using the `<para>` tag.

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

## &lt;c&gt; and &lt;code&gt; tags

To insert a single line of code, or inline code, `<c>just put the code between these</c>`

To create a code block

```csharp
<code>
	Put the code
	in
	a code block  
<code>
```

## &lt;example&gt; tag

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

## &lt;returns&gt; tag

The `<returns>` content should be short, and contained to a single line.

Example:

```csharp
/// <returns>A boolean value.</returns>
```

## &lt;value&gt; tag

The `<value>` tag defines a value for something.

Example:

```csharp
/// <value>Default value is <c>false</c></value>
```

# XML documentation example

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

***

<div align="center">

This document is part of the [Abatab Documentation Project](https://spectrum-health-systems.github.io/Abatab-Documentation-Project/).  

Last updated: **November 1, 2023**
  
</div>