<div align="center">
	<img src="_attachments/Logo/AbatabDocumentationProjectLogo.png">
		<h1>
			The Abatab Documentation Project
	</h1>
</div>

***

# About The Abatab Documentation Project

The Abatab Documentation Project is a living document for [Abatab](https://github.com/spectrum-health-systems/Abatab).

The goal of the Abatab Documentation Project is to provide useful documentation for Abatab development purposes, including:

- Documentation on configuring and deploying Abatab
- Documentation and guidelines for developing Abatab
- [API documentation](https://spectrum-health-systems.github.io/Abatab/)
- TBD

The best way to view the Abatab Documentation Project is via the repository [GitHub Pages](https://spectrum-health-systems.github.io/Abatab-Documentation-Project/).

# Development

The Abatab Documentation Project is developed using [Obsidian.md](https://obsidian.md/) with the following plugins:

- [Advanced Tables](https://github.com/tgrosinger/advanced-tables-obsidian)
- [Webpage HTML Export](https://github.com/KosmosisDire/obsidian-webpage-export)

The Abatab Documentation Project also utilizes [Mermaid](https://mermaid.js.org/)).

The development source files can be found [here](https://github.com/spectrum-health-systems/Abatab-Documentation-Project/tree/development/Abatab%20Documentation).

# Release

The Abatab Documentation Project release process is as follows:

<div align="center">

  ```mermaid
  graph LR

      Deploy[Deploy] --> Merge[Merge] --> Publish[Publish]
  ```
</div>

## Deploy

1. Click the **Webpage HTML Export** icon
![](_attachments/Documentation_Export/WebpageHTMLExport_01.png)

2. Confirm that all necessary files/folders are included
![](_attachments/Documentation_Export/WebpageHTMLExport_02.png)

3. Confirm that the export folder is ***docs/***
![](_attachments/Documentation_Export/WebpageHTMLExport_03.png)

4. Click **Export**
![](_attachments/Documentation_Export/WebpageHTMLExport_04.png)

## Merge branches

Just merge the development branch with the main branch!

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
