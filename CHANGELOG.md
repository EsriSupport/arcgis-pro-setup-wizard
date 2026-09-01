# Changelog

Every released version of the ArcGIS Pro Setup Wizard, newest first.

Versions are `MAJOR.MINOR.PATCH`: MAJOR for a release that changes what the
wizard is to the people using it, MINOR for behaviour you would notice, PATCH
for fixes alone. Each build also carries a build stamp, shown along the bottom
of every screen — quote the whole line when contacting support.

---

## 2.0.0

First public release.

When the wizard checks for updates and finds it is already the newest version,
the line along the bottom ends "- latest". If it cannot reach GitHub it says
nothing rather than claiming to be up to date.

## 1.16.0

Checks on startup whether a newer version of the wizard has been published, and
offers it on the welcome screen with a note of what changed. The check runs in
the background, never delays the window, and stays silent if the computer has
no internet connection. Nothing is sent but the request itself.

## 1.15.1

Fixed: the welcome screen could show a message that belonged to the next
screen ("No ArcGIS Pro setup file in this folder").

## 1.15.0

Where the setup file is an extracted `.msi`, the wizard now reads the
requirements built into the package itself and refuses the installation if the
package would refuse this computer — quoting Esri's own message.

The readiness screen is easier to read: no row is selected by default, so the
colour-coded status of each row stays visible, and anything blocking the
installation is named in a band above the table as well as in the table. The
explanation panel now summarises the whole screen until you select a row.

## 1.14.0

An ArcGIS Pro version newer than the wizard is now clearly marked as such: the
requirements it checks against are labelled "assumed", and it says which
earlier version they came from, instead of reporting a confident pass.

## 1.13.0

Checks that this computer can run the ArcGIS Pro version selected — Windows
edition and build, memory and processors — and stops the installation if it
cannot, naming the newest version the computer can run.

Worth knowing: Windows 10 support ends at ArcGIS Pro 3.5. Both 3.6 and 3.7
require Windows 11.

## 1.12.0

The installing screen now shows how far along it is and roughly how much time
is left, measured from the work actually done rather than guessed. The estimate
appears only once there is enough progress to base it on, and is withdrawn if
progress stops.

## 1.11.0

ArcGIS Pro's optional components — Create Locator, Semantic Search, Tool
Suggestions — can be chosen before installing. Where the setup file is an
extracted `.msi`, the list comes from the package itself.

## 1.10.0

Each build now carries a version and a build stamp, shown on every screen, so a
screenshot identifies exactly which build is running.

## 1.9.0

Patches for other ArcGIS Pro versions are no longer listed at all. Only those
that apply to the version being installed are shown; the rest are counted and
explained underneath.

## 1.8.1

The rule that matches patches to a version now handles every ArcGIS Pro
numbering, including double-digit patch numbers such as 3.5.10.

## 1.8.0

Patches are matched to the ArcGIS Pro version being installed. Previously a
folder holding patches for several versions offered all of them, whichever
setup was chosen.

Fixed: the emblem could smear and take several seconds to redraw when the
window was resized; text could be cut off until the window was widened.

## 1.7.0

Reduced to a single executable and a README written for someone who has never
installed ArcGIS Pro.

## 1.6.0

Ownership and version shown in Esri's form along the bottom of every screen.

## 1.5.0

Added the welcome screen.

## 1.4.0

The owning team is named on every screen.

## 1.3.0

Esri's look and conventions throughout: colours, the globe emblem, and standard
wizard buttons. The executable now carries its product name, company and
version in its file properties. The Stop button explains what stopping does
before it does it, and download links for missing prerequisites are shown in
full.

## 1.2.0

The Esri North Africa logo as the application icon.

## 1.1.1

Fixed: the Browse button could be positioned off the edge of the window.

## 1.1.0

The setup files can live in any folder: browse to it, type or paste a path, or
drag a folder onto the window.

## 1.0.0

First release. Scans a folder for the ArcGIS Pro setup, its prerequisites and
any patches; checks what this computer already has and skips it; then installs
what is missing — prerequisites, ArcGIS Pro, then patches in Esri's order.
