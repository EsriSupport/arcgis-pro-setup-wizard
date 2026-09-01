# Changelog

Every released version of the ArcGIS Pro Setup Wizard, newest first.

Versions are `MAJOR.MINOR.PATCH`: MAJOR for a release that changes what the
wizard is to the people using it, MINOR for behaviour you would notice, PATCH
for fixes alone. Each build also carries a build stamp, shown along the bottom
of every screen — quote the whole line when contacting support.

---

## 2.2.7

Files belonging to an ArcGIS Pro extension are no longer mistaken for ArcGIS
Pro's own.

Esri names an add-on after the product it extends, so Reality Studio arrives as
`ArcGISPro_34_Reality_Ext_192545.exe` with a patch called
`ArcGISPro_341_Reality_Ext_192546.msp`. The wizard was offering that setup as a
version of ArcGIS Pro to install, and offering its patch **whatever** version
you chose — it could not read a version out of a name in that shape, and a
patch with no version was treated as belonging to all of them.

The rule now is that ArcGIS Pro's own files carry nothing after the name but a
version and a build number. A word in there means the file belongs to something
else, so it is left out — and the note beneath the patch list says one was left
out, rather than dropping it in silence.

The check that a patch belongs to the version being installed is now made where
the installation plan is built, as well as on the page that lists them.

## 2.2.6

Findings from a second pass over every screen.

The last screen, after a preview run, told you to "run this app again as
Administrator with the preview box unticked" — a checkbox removed from the
wizard some time ago. It now says what is actually true: start it again and
choose Yes when Windows asks for permission.

The components window has caught up with the rest of the app: its title bar is
Esri blue rather than whatever accent colour the computer is set to, it no
longer carries a stray icon, and a component's description is written in the
ordinary text colour instead of the blue that means "you can click this".

The update button is the last one in the wizard to gain an access key.

## 2.2.5

Installing an earlier ArcGIS Pro over a later one is now stopped rather than
described as an upgrade.

Choosing ArcGIS Pro 3.5 on a computer running 3.7 was reported as "this will
upgrade the existing one" and allowed to start. It is a step backwards, not an
upgrade, and ArcGIS Pro cannot be moved back to an earlier release in place —
the setup will not install over a later version. The row now reads **Uninstall
3.7 first** and says what to do instead: uninstall ArcGIS Pro, then run the
wizard again.

A genuine upgrade is unchanged, and now says which way it goes — "Upgrade 3.7
to 3.10" rather than "Install 3.10 over 3.7". Version numbers are compared as
numbers, so 3.10 is correctly newer than 3.7.

## 2.2.4

Patches the computer already has are no longer applied a second time.

ArcGIS Pro records its patch level in its own version: 3.7.1.1904 means patch
3.7.1 went on long ago. The wizard was offering that patch again anyway,
costing twenty minutes and ending in "not applicable". Where the base
installation is being skipped because the right version is already there, any
patch the installed version already covers is now skipped too, and the row says
so.

Newer patches are unaffected — a 3.7.2 patch still goes on over 3.7.1. Ticking
the box that reinstalls ArcGIS Pro puts the base version back and every patch
with it, which is the way to apply one again deliberately.

## 2.2.3

Cancel and Escape now ask before throwing anything away.

Once past the welcome screen, closing the wizard — by the Cancel button, by
Escape, by the window's X, or by Alt+F4 — asks first, with **No** as the
default. Escape in particular is a key people press to dismiss things, and
since 2.2.0 it has been able to close the wizard; it should not have been able
to discard a chosen folder, patches and components without a word. The welcome
screen still closes without asking, because nothing has been chosen there yet.

Nothing changes during an installation: that was already protected, and still
is. Stop asks for confirmation, waits for the current step to finish, and
closing the window outright is refused.

**Fixed:** in the components window, "Use standard" wrote straight through to
the selection, so opening it, pressing that, and then pressing Cancel changed
the components anyway. Nothing leaves that window now except through **Use
these components**.

## 2.2.2

The arrow on the release notes button now points the way the panel moves.

The notice sits at the bottom of the window and grows upward, so **What's new**
carries an up arrow and **Hide notes** a down one — the way a drawer handle
works. It had them the other way round, following the convention for a panel
that drops its content below the button, which is not what this one does.

## 2.2.1

The release notes panel was the one screen the design pass missed.

Paragraph breaks in the notes were being collapsed, so what should have been
readable paragraphs arrived as a wall of text. The panel can now be reached and
scrolled from the keyboard, **What's new** has an access key like every other
button, and it shows whole lines rather than slicing one through the middle.

## 2.2.0

A design pass over every screen.

**Keyboard.** Enter now moves the wizard on and Escape cancels, on every page.
Every button has an access key — Alt+N for Next, Alt+B for Back, Alt+R for
Re-check, and so on — so the whole wizard can be driven without a mouse.

**The title bar is Esri blue** on Windows 11 instead of whatever accent colour
the computer happens to be set to.

**The table of checks is readable at any window size.** "Required" and "On this
computer" had fixed widths and so were cut short however wide the window was;
every column now takes a share of the space. Hovering a row shows the whole of
it, so a narrow window is never a dead end.

**Nothing is lost on a small window.** At the smallest size the wizard allowed,
the list of what it was about to do collapsed to a single line. The table and
that list now share the height between them.

**Next waits for a setup file.** On an empty folder it used to lead to a page of
green ticks measured against a version nobody had chosen.

**Colour.** Three pieces of text were below the accessibility standard for
contrast and have been darkened. "Will install" no longer uses the same blue
that means "you can click this" everywhere else, and the preview notice is now
informational blue rather than warning amber.

**Smaller things.** Found and missing files are marked with a tick and a dash
rather than plus and minus; the folder path shows in full on hover; captions are
no longer smaller than the text they label; an empty patch list no longer stands
as a large empty box; the components window can be resized and its button says
what it does.

## 2.1.2

The Install button is no longer offered when there is nothing to install.

Where ArcGIS Pro and everything it needs are already on the computer, Install
is now unavailable and the reason is written beside it — "ArcGIS Pro 3.7 is
already installed. Tick the box to install it again." Pressing it used to be
allowed, and answered with a message box saying there was nothing to do. The
summary now describes the reinstall too, instead of still reporting that
nothing is left to install.

The note along the bottom of the window also widens with the window, so a
longer message is no longer cut short.

## 2.1.1

Appearance fixes on the "Before installing" screen and the update notice.

The table of checks had no top border: the message above it was tall enough to
cover it. The download button now sizes itself to what it says, so a caption
like "Download .NET 6.0 (x64)" no longer wraps across two lines inside it. The
update notice no longer repeats which version you are running — that is already
along the bottom of every screen — and its buttons now sit level with the text
whether the notes are open or closed. Release notes that were hard-wrapped when
they were written are re-flowed to the width of the panel instead of breaking
mid-sentence, and each version's notes are now indented as a block beneath the
version number — wrapped lines included — with the version itself in bold, so
the two can be told apart at a glance.

## 2.1.0

The update notice can now show everything that changed since the version you
are running.

Closed, it says only that an update exists and gives its number. A **What's
new** button opens the release notes for every version published since yours —
not only the newest one — so someone several versions behind can see all of it
and decide whether the update is worth the interruption. The button closes it
again, and the notes are fetched only when it is opened.

## 2.0.2

The update prompt no longer cuts its own text off mid-sentence.

It shows the first line of the release notes, shortened with an ellipsis to
whatever the window is wide enough for, and the notes in full when the pointer
rests on them.

## 2.0.1

The update prompt now downloads the new version directly when you click it,
rather than opening a page first.

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
