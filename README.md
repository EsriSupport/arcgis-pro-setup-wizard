# ArcGIS Pro Setup Wizard

Installs ArcGIS Pro — any version — together with the prerequisites that
version needs and any patches you have, in the right order, without a command
line.

Made and maintained by the **Esri North Africa Technical Support Team**.

## Download

Get the latest release from the [Releases page](../../releases/latest) and run
`ArcGISProSetupWizard.exe`. It is a single file: nothing to install, and no
runtime to add first.

## What it does

ArcGIS Pro needs particular Microsoft components before it will run, and the
versions differ from one ArcGIS Pro release to the next. Getting that wrong is
the usual reason an installation fails. The wizard:

- reads the ArcGIS Pro setup, prerequisites and patches out of a folder you
  point it at
- checks whether this computer can run the version you chose — Windows
  edition, memory and processors — and stops you if it cannot, naming the
  version that would work instead
- checks what is already installed and skips whatever is already correct
- installs what is missing: prerequisites, then ArcGIS Pro, then patches in
  the order Esri intends
- applies only the patches that belong to the version being installed

Optional ArcGIS Pro components — Create Locator, Semantic Search, Tool
Suggestions — can be turned on before installing, so there is nothing to run
afterwards.

## What you need

- Windows 10 or 11, 64-bit
- Permission to install software (an administrator password)
- Your ArcGIS Pro download from My Esri, and any patch files you were given

## First run

Windows may show a blue "Windows protected your PC" box, because this app is
not code-signed. Click **More info**, then **Run anyway**. To check what you
are running first: right-click the file, choose Properties, then Details — it
should read *ArcGIS Pro Setup Wizard, Esri North Africa*.

## Support

Problems, or an ArcGIS Pro release the wizard does not recognise yet: contact
the Esri North Africa Technical Support Team. The last screen of the wizard
has a button that opens the folder with the log files — attach those.

## History

Every release and what changed in it: [CHANGELOG.md](CHANGELOG.md).

---

© 2026 Esri North Africa – Technical Support Team. All rights reserved.
ArcGIS and Esri are trademarks of Environmental Systems Research Institute, Inc.
