<!-- 
	Abatab Documentation Project: Releases
	Last updated: 231030
	This documentation is incomplete.
-->

<div align="center">

![](_attachments/AbatabDocumentationProjectLogo.png)
	<h1>
		Releases
	</h1>
</div>

***

# Releasing a new development branch

- When commiting, the subject should be the simple build number (`bYYMMDDD`)
	- Example: `b231030`

# Releasing a new main branch

- Modify Abatab/README.md details
	- Modify version
	- Remove development note
- Modify Abatab/Abatab.asmx.cs header details
	- Modify version
	- Remove development note
- Change the version number in Abatab.asmx.cs
	- `public string GetVersion() => "VERSION YY.MM";
	- Only changed when releasing new main branches, since the Community Release is based on the main branch
- Modify AppData/Version.json (TODO)

# Releasing a new Community Release

- Modify Abatab/README.md details
	- Change version
	- Remove Community Release note
- Modify Abatab/Abatab.asmx.cs header details
	- Change version
	- Remove Community Release note
- Modify AppData/Version.json (TODO)