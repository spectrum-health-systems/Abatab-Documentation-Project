<div align="center">

![](_attachments/logo/abatab-documentation-project-logo.png)

</div>

***

# Releasing a new Development Release

## Development branch

### New development branch

- Modify version number in:
	- Abatab.GetVersion()
	- Abatab/README.md
	- AssemblyInfo.cs files
	- Settings.settings
- When committing to GitHub, the subject should be the simple build number (`bYYMMDDD`)
	- Example: `b231030`

## Main branch

- Copy DocFX/site_ to Abatab/docs
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

<br>
<br>

***

<div align="center">
	<h6>
		This document is part of the <a href="https://spectrum-health-systems.github.io/Abatab-Documentation-Project/">Abatab Documentation Project</a>
		<br>
		<sub style="color:DarkSlateGrey;">
			Last updated: <b>November 6, 2023</b> [b231106.1057]
		</sub>
	</h6>
</div>