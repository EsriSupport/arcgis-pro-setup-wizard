# Changelog

Every released version of the ArcGIS Pro Setup Wizard, newest first.

Versions are `MAJOR.MINOR.PATCH`: MAJOR for a release that changes what the
wizard is to the people using it, MINOR for behaviour you would notice, PATCH
for fixes alone. Each build also carries a build stamp, shown along the bottom
of every screen — quote the whole line when contacting support.

---

## 2.3.0

Searching a whole drive, and a clearer way to choose between what it finds.

- New: searching a large folder no longer freezes the window. A panel shows the folders counted so far and where it has reached, with a Stop button
- New: while a search runs, the folder box shows the folder being searched and the folder row is unavailable - Stop is the way to search somewhere else
- New: setup files show where they came from, so identical copies in different folders can be told apart
- The list of setup files is a table with columns for the version, the file and its location, replacing a dropdown that covered the page beneath it and could show only one at a time
- Fixed: Windows keeps its own cached .msp files, and those were being read as ArcGIS Pro patches - one was reported as "ArcGIS Pro 7.2.8", a version that does not exist
- Fixed: the same patch found in several folders was queued once for each copy, so it was applied several times over; only the first is used and the rest are counted
- Fixed: a horizontal scrollbar appeared under the setup table for no reason and went away when used
- Fixed: scrolling the setup table and then choosing a row could leave the table showing an empty box
- The patch list is hidden when no setup file has been chosen, since there is nothing for patches to go on
- The summary counts what was found - "9 found - choose one below", "6 of 14 apply to ArcGIS Pro 3.5" - and no longer repeats what the table below already says
- The note under the patch list is one line; what was left out, and why, is on the summary row

## 2.2.9

The What's new panel understands a bulleted release note.

- Fixed: it knew the bullet characters markdown uses but not the round bullet people type, so a note written that way arrived as one long paragraph
- Round, middle and hollow bullets and en and em dashes each start a line of their own

## 2.2.8

The patch list is as tall as the patches in it.

- Fixed: the list was laid out before it was filled, so three patches went into a box built for none, with a scrollbar and an empty page beneath
- It now grows a row at a time, between one row and the room available
- Fixed: while installing, the line under the progress bars relayed Windows Installer's own diagnostics - text like "Note: 1: 2205 2: 3: _RemoveFilePath" reads like a failure; the log below keeps every line
- The wizard's prompts wear the same Esri blue title bar as the wizard itself

## 2.2.7

An extension's files are no longer mistaken for ArcGIS Pro's own.

- Fixed: Reality Studio ships as ArcGISPro_34_Reality_Ext_192545.exe and was offered as a version of ArcGIS Pro to install
- Fixed: its patch was offered whatever version you chose, because no version number could be read from a name in that shape
- ArcGIS Pro's own files carry nothing after the name but a version and a build number; a word in there means the file belongs to something else
- The note beneath the patch list says when a file has been left out, rather than dropping it in silence

## 2.2.6

Wording and appearance fixes.

- Fixed: after a preview run, the last screen told you to untick a preview box that had been removed from the wizard
- Fixed: a component's description was written in the blue that means "you can click this"
- The components window's title bar is Esri blue rather than the computer's accent colour, and it no longer carries a stray icon
- The update button has an access key

## 2.2.5

Installing an earlier ArcGIS Pro over a later one is stopped.

- Fixed: choosing 3.5 on a computer running 3.7 was reported as an upgrade and allowed to start
- ArcGIS Pro cannot be moved back to an earlier release in place: uninstall ArcGIS Pro first, then run the wizard again
- A genuine upgrade now says which way it goes - "Upgrade 3.7 to 3.10"
- Version numbers are compared as numbers, so 3.10 is correctly newer than 3.7

## 2.2.4

Patches the computer already has are no longer applied a second time.

- Fixed: ArcGIS Pro 3.7.1.1904 already includes patch 3.7.1, and the wizard offered it again - twenty minutes ending in "not applicable"
- Any patch the installed version already covers is skipped, and the row says so
- Newer patches are unaffected: a 3.7.2 patch still goes on over 3.7.1
- Ticking the box that reinstalls ArcGIS Pro puts the base version back and every patch with it

## 2.2.3

Cancel and Escape ask before discarding anything.

- Past the welcome screen, closing the wizard - by Cancel, by Escape, by the window's X or by Alt+F4 - asks first, with No as the default
- The welcome screen still closes without asking, because nothing has been chosen there yet
- Installation is unchanged: Stop asks for confirmation, waits for the current step to finish, and closing the window outright is refused
- Fixed: "Use standard" in the components window wrote straight through to the selection, so Cancel afterwards did not undo it

## 2.2.2

The arrow on the release notes button points the way the panel moves.

- Fixed: the arrows were the other way round, following the convention for a panel that drops its content below the button
- The notice sits at the bottom of the window and grows upward, so What's new carries an up arrow and Hide notes a down one

## 2.2.1

Fixes to the release notes panel.

- Fixed: paragraph breaks were collapsed, so notes arrived as a wall of text
- Fixed: the panel sliced its last line through the middle rather than showing whole lines
- The panel can be reached and scrolled from the keyboard
- What's new has an access key, like every other button
- The documentation that ships with the wizard now covers the keyboard shortcuts and the update check

## 2.2.0

Keyboard control, an Esri blue title bar, and a screen that holds together at any window size.

- New: Enter moves the wizard on and Escape cancels, on every page
- New: every button has an access key - Alt+N for Next, Alt+B for Back, Alt+R for Re-check
- The title bar is Esri blue on Windows 11 rather than whatever accent colour the computer is set to
- Fixed: "Required" and "On this computer" had fixed widths and were cut short however wide the window was; every column now takes a share of the space, and hovering a row shows the whole of it
- Fixed: at the smallest size the wizard allowed, the list of what it was about to do collapsed to a single line
- Fixed: Next led to a page of green ticks when no setup file had been chosen
- Fixed: three pieces of text were below the contrast standard for readability
- "Will install" no longer uses the same blue that means "you can click this", and the preview notice is informational blue rather than warning amber
- Found and missing files are marked with a tick and a dash rather than a plus and a minus
- The folder path shows in full on hover, and an empty patch list no longer stands as a large empty box
- The components window can be resized, and its button says what it does

## 2.1.2

Install is no longer offered when there is nothing to install.

- Fixed: pressing Install with everything already in place was allowed, and answered with a message box saying there was nothing to do
- Install is now unavailable, with the reason beside it: "ArcGIS Pro 3.7 is already installed. Tick the box to install it again."
- Fixed: the summary still said nothing was left to install after a reinstall had been ticked
- The note along the bottom widens with the window, so a longer message is not cut short

## 2.1.1

Appearance fixes on the Before installing screen and the update notice.

- Fixed: the table of checks had no top border - the message above it was tall enough to cover it
- Fixed: a caption like "Download .NET 6.0 (x64)" wrapped across two lines inside its button; the button now sizes itself to what it says
- Fixed: release notes hard-wrapped when they were written broke mid-sentence instead of re-flowing to the panel
- The update notice no longer repeats which version you are running - that is already along the bottom of every screen
- Notice buttons sit level with the text whether the notes are open or closed
- Each version's notes are indented beneath the version number, wrapped lines included, with the version in bold

## 2.1.0

See everything that changed since the version you are running.

- New: a What's new button opens the release notes for every version published since yours, not only the newest one
- Closed, the notice says only that an update exists and gives its number
- The notes are fetched when the button is opened, so startup is not delayed

## 2.0.2

The update prompt no longer cuts its own text off mid-sentence.

- Fixed: the note beside the version ran past the edge of the window
- It now shows the first line of the release notes, shortened to the width available
- The notes in full appear when the pointer rests on them

## 2.0.1

The update prompt downloads the new version directly.

- Clicking it starts the download instead of opening a page first

## 2.0.0

First public release.

- Installs ArcGIS Pro with the prerequisites that version needs and any patches you have, in the order Esri intends
- Checks what is already on the computer and skips whatever is already correct
- Stops the installation if the computer cannot run the version chosen, and names the version that would work instead
- Applies only the patches that belong to the version being installed
- Optional components - Create Locator, Semantic Search, Tool Suggestions - can be turned on before installing
- Checks for a newer wizard at startup; the line along the bottom ends "latest" when it is current, and says nothing at all when GitHub cannot be reached

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
