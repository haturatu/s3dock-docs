---
title: "Supported file formats"
description: "Image, video, audio, and document types S3Dock recognizes."
toc: true
---

S3Dock recognizes file types by extension to choose icons, previews, and viewers. The lists below are the types the app treats as media or documents.

## Images

Previewed with the built-in image viewer and used for thumbnails:

- `jpg`, `jpeg`
- `png`
- `webp`
- `gif`
- `heic`

## Videos

Played with the in-app Media3 ExoPlayer screen and shown with generated thumbnails:

- `mp4`, `m4v`
- `webm`
- `mkv`
- `mov`
- `avi`
- `3gp`

## Audio

Recognized for icons and the Music library (including background playback and smart library tags):

- `mp3`
- `m4a`
- `ogg`
- `wav`
- `flac`

## Documents

Shown in the Documents tab and scanned by extension:

- Text: `txt`, `md`
- PDF: `pdf`
- Office: `doc`, `docx`, `xls`, `xlsx`, `ppt`, `pptx`
- Tables: `csv`, `tsv`

## Notes

- Files with other extensions still appear in the Files tab and can be uploaded, downloaded, moved, and shared; they simply will not get a media preview or be grouped into a media library.
- Media library tabs (Photos, Videos, Music, Documents) filter scanned folders by these extensions. A scanned folder containing only unsupported types will appear empty in that tab.
- The Music smart library reads artist, album, track, and cover metadata from the audio files above when Smart Music Library is enabled.
