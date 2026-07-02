---
title: "Usage"
description: "How to set up and use S3Dock."
toc: true
---

This page explains the basic setup flow for S3Dock.

## Before you start

S3Dock does not create a storage account for you. Prepare an object storage bucket and credentials from your provider first.

You usually need:

- Endpoint URL
- Bucket name
- Access key ID
- Secret key
- Region, if your provider requires it
- Path-style URL setting, if your provider requires it

For Cloudflare R2, MinIO, Wasabi, Backblaze B2, DigitalOcean Spaces, Amazon S3, and many other S3-compatible providers, the app can start from a preset and then you can edit the values.

## First launch

When no storage connection is configured, S3Dock opens with a simple setup screen.

<figure class="s3dock-phone-shot">
  <img src="/usage/initial-setup.png" alt="S3Dock first launch setup screen">
  <figcaption>Use Add storage to create a new connection, or Restore backup if you are moving from another device.</figcaption>
</figure>

Choose one of these actions:

- **Add storage**: open Storage settings and enter a new provider or bucket.
- **Restore backup**: import an app database backup created by S3Dock.

## Add a storage connection

Tap **Add storage** on the first screen. S3Dock opens Settings > Storage.

<figure class="s3dock-phone-shot">
  <img src="/usage/storage-overview.png" alt="S3Dock Storage settings overview">
  <figcaption>The Storage page shows connection status, saved providers, saved buckets, cache usage, and scan folder status.</figcaption>
</figure>

If this is a fresh install, the page will show that no provider or bucket is saved yet.

## Choose a provider preset

Scroll to **Connection editor** and choose a provider preset. You can search providers when the list is long.

<figure class="s3dock-phone-shot">
  <img src="/usage/provider-presets.png" alt="S3Dock provider preset list">
  <figcaption>Choose Cloudflare R2, Amazon S3, MinIO, Wasabi, Backblaze B2, DigitalOcean Spaces, or Custom Object Storage Provider.</figcaption>
</figure>

Use **Custom Object Storage Provider** when your provider is S3-compatible but not listed.

## Enter connection details

After choosing a preset, fill in the connection fields.

1. Enter the endpoint.
2. Enter the bucket name.
3. Enter the access key ID.
4. Enter the secret key.
5. Set region only when needed.
6. Enable path-style URLs only when needed.
7. Tap **Save and Connect**.

S3Dock trims accidental spaces and line breaks from connection fields, but you should still copy values carefully from your provider dashboard.

## Restore from backup

Use **Restore backup** on the first screen when you already exported an app database backup from S3Dock.

Database backup is intended for app migration. If you choose a plaintext backup export, connection credentials are included in plaintext so they can be restored on another device. Store that file carefully and delete it when it is no longer needed.

## Browse files

After a successful connection, the **Files** tab shows the current bucket folder.

Common actions:

- Use search to filter the current folder.
- Use the view button to switch between list, grid, and masonry views.
- Use sort to change name, modified date, or size order.
- Tap folders to navigate.
- Tap images, videos, or music to open the media viewer.
- Use the plus button to upload files, upload folders, create folders, or import from camera.

## Media libraries

Photos, Videos, Music, and Documents can scan selected bucket folders. If no scan folder is configured, open the tab and choose a bucket folder to scan.

Music also supports a smart library mode for songs, artists, albums, and folder-based browsing when metadata is available.

## Offline files and cache

Use **Keep Offline** from a file menu to store a file locally for later use. The Offline tab lists saved files. Cache limits and clear actions are available from Settings.

## Security notes

- HTTPS endpoints are recommended.
- HTTP endpoints should only be used on trusted local networks.
- External apps receive a short-lived signed URL when you choose Open with.
- Do not share exported backups that include credentials.
