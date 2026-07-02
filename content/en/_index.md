---
title: "S3Dock"
description: "Android client for object storage."
eyebrow: "Android client for object storage"
lead: "Turn your own object storage bucket into a practical Android cloud drive with file browsing, media preview, uploads, offline access, and direct provider control."
primaryAction: "Privacy Policy"
toc: true
---

Turn your own object storage bucket into a practical Android cloud drive with file browsing, media preview, uploads, offline access, and direct provider control.

## Built for user-owned storage

S3Dock does not provide a cloud account. You connect your own Amazon S3, Cloudflare R2, MinIO, Wasabi, Backblaze B2, DigitalOcean Spaces, or another S3-compatible object storage endpoint.

This is useful when a normal cloud drive plan does not match how you store files. Object storage lets you choose the provider, bucket, region, and pricing model instead of being locked into one fixed consumer cloud service.

{{< cards >}}
  {{< card title="Browse and manage" icon="folder" subtitle="Use list, grid, and masonry layouts with search, sorting, favorites, uploads, downloads, move, rename, and delete operations." >}}
  {{< card title="Media previews" icon="photograph" subtitle="Open photos, videos, and music with built-in viewers, thumbnails, cache controls, and background audio playback." >}}
  {{< card title="Offline access" icon="cloud-download" subtitle="Keep selected files available offline and control local cache usage from the app settings." >}}
{{< /cards >}}

## Demo and screenshots

The short demo below shows S3Dock being used as a mobile file manager for an object storage bucket.

<div class="s3dock-demo-video">
  <iframe src="https://www.youtube.com/embed/WSmvRj0nJXc" title="S3Dock Android app demo" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

<div class="s3dock-screenshot-grid">
  <figure>
    <img src="/showcase/app-files.webp" alt="S3Dock file browser showing folders in a bucket">
    <figcaption>Browse bucket folders with search, sorting, view switching, and file actions.</figcaption>
  </figure>
  <figure>
    <img src="/showcase/app-media.webp" alt="S3Dock grid view with upload actions">
    <figcaption>Use grid view, folder previews, and expandable upload actions.</figcaption>
  </figure>
  <figure>
    <img src="/showcase/app-settings.webp" alt="S3Dock masonry photo view">
    <figcaption>Preview image-heavy folders with a masonry layout.</figcaption>
  </figure>
</div>

## Why use object storage as a drive?

Many cloud drives are convenient, but they can be awkward for large personal archives, media folders, or PC-to-phone file exchange. You may pay for a large plan even when you only use part of it, hit upload limits, wait on slow bulk transfers, or find it difficult to move everything to another service later.

With an object storage bucket, you can keep the storage layer independent:

{{< cards >}}
  {{< card title="Control the provider" icon="server" subtitle="Use R2, MinIO, Wasabi, B2, Spaces, Amazon S3, or another compatible endpoint. Switch providers by changing the connection settings instead of changing the whole app workflow." >}}
  {{< card title="Works with desktop tools" icon="terminal" subtitle="The same bucket can be mounted or synchronized from Linux, macOS, or Windows with tools such as Rclone, while S3Dock gives you a mobile file manager on Android." >}}
  {{< card title="Choose a region" icon="globe-alt" subtitle="Select a nearby or cost-effective region when your provider supports it. This can improve latency for previews, uploads, and media playback." >}}
{{< /cards >}}

<figure class="s3dock-wide-shot">
  <img src="/showcase/r2-usage.webp" alt="Example Cloudflare R2 usage summary">
  <figcaption>Object storage services such as Cloudflare R2 can be practical for personal archives when their pricing, region, and request model fit your workload.</figcaption>
</figure>

## What S3Dock is good at

- Managing files in buckets without a developer-operated file server
- Previewing photo and video folders from object storage
- Playing music from your bucket, including background audio playback
- Keeping selected files offline for travel or unstable networks
- Using multiple providers and buckets from one app
- Importing and exporting app settings or database backups when moving devices

## Designed for realistic storage workflows

S3Dock is intended for people who already use object storage or want to use it as a more flexible personal cloud. It keeps the S3-compatible bucket structure visible, but adds mobile-friendly views such as Photos, Videos, Music, Documents, Favorites, Offline, Transfers, grid view, masonry view, search, sorting, and folder previews.

## Privacy-first architecture

The app connects directly from your Android device to the storage endpoint you configure. S3Dock does not operate a developer-controlled server for your files or credentials.

Connection details stay on your device unless you explicitly export a backup that includes them. If you open a private file in another app, S3Dock uses a short-lived signed URL so the selected app can access that file temporarily.
