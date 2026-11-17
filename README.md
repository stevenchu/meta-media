# Meta Media

Meta Media lets you copy, paste, and edit dates, times, and GPS locations in photos and videos on your Mac.

Inspired by the easy metadata copying in iOS Photos, it brings that convenience to files in Finder—especially when compression or conversion strips away their original details.

## Requirements

- Mac with Apple silicon (M1 or newer)
- macOS 14 Sonoma or later
- Free to use; no account required

This initial release is not Apple-notarized. macOS may block its first launch; some managed Macs may prohibit it. Download only from this project's official releases. If you choose to open it, follow Apple's per-app instructions: https://support.apple.com/102445. You should never need to disable Gatekeeper globally or paste security-bypass commands into Terminal.

## Install

1. [Download the ZIP from Releases](https://github.com/stevenchu/meta-media-releases/releases/latest) and unzip it.
2. Move **Meta Media.app** into Applications (or your user's Applications folder).
3. Open Meta Media.
4. For Finder integration, choose **Meta Media → Install Finder Quick Action…**.
5. Right-click a media file → **Quick Actions → Copy/Paste Media Metadata…**. If missing, use Quick Actions → Customize… to enable it.

If you move or rename the app later, reinstall the Finder action from the same menu. Sparkle updates that replace the app at the same location keep the installed action working.

## Use

Drop files onto the app or choose Add files. Edit date, time, or location directly in the right panel. Valid changes save to the original file automatically. Each section offers Undo during the current app session.

When capture metadata is missing, the date fields show a labeled Finder Created or Modified fallback. Add a location by searching, pasting coordinates, or choosing a recent or saved place.

Select a range with Shift-click or toggle individual files with Command-click or Control-click. To bulk paste in the app, copy a property, select the targets, then right-click any selected row and choose the matching Paste command. Renames and same-drive moves update open rows. Missing files are dimmed and editing pauses until they’re available again.

Copy date/time or location from a section header, or right-click a file in the desk list. The Finder action copies available metadata from one source, then lets you paste date/time, location, or both to selected files. When no capture date exists, Finder Copy uses filesystem Created and Modified dates. Missing source location never clears the destination's location.

**Try it on copies first.** Changes modify the file itself. Undo is session-only; Finder Quick Action changes have no app Undo history. Keep your own backups. Delete in the app only removes files from its desk list, not from disk.

## Supported formats

| Format | Metadata editing |
| --- | --- |
| JPEG, PNG, HEIC/HEIF, WebP | Read and write |
| MP4, MOV | Read and write |
| DNG | Read/copy only |
| Other formats | Not guaranteed; the app identifies read-only files |

Time is displayed in AM/PM. Capture-date edits synchronize Finder Created and Modified. Without GPS, time uses your device zone; with GPS, it uses the location's zone when available. If zone lookup fails, the app shows its fallback. Manual offset is available for ambiguous times.

## Updates

Choose **Meta Media → Check for Updates…**. Sparkle verifies signed update archives and handles download, installation, and relaunch. Automatic checks are optional. Updates may require authorization if the installation folder isn't writable.

End users never need the developer's private update-signing key. A Keychain prompt mentioning “Private key for signing Sparkle updates” belongs to the developer's release tools, not normal app use.

## Privacy

Media editing happens locally; the app does not upload your photos or videos. Apple Maps search, map display, and time-zone lookup use Apple services. Update checks contact the release host. Saved locations stay on your Mac. Dependency license notices ship inside the app.

## Known limitations

- Apple silicon only; Intel builds are not included.
- First-install/quarantine behavior still needs validation on another Mac.
- Batch writes are verified per file, not one transaction for the whole batch.
- Finder edits made to a file already open in Meta Media require reimporting that file.
- Saved locations and undo are separate: changing a saved place does not retag existing files.

For a bug report, include macOS/app version, file format, steps, and the error text. Avoid uploading private media or exact GPS coordinates; use a non-sensitive sample if one is needed.
