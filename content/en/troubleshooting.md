---
title: "Troubleshooting & FAQ"
description: "Common S3Dock setup problems and how to fix them."
toc: true
---

This page covers the most common issues when connecting S3Dock to object storage.

## Connection fails or is rejected

- **Check the endpoint scheme.** S3Dock requires `https://` by default. If your provider uses plain HTTP (for example a local MinIO or NAS), enable **Allow insecure HTTP endpoints** in Settings > Network / Object Storage, then reconnect.
- **Trim copy-paste errors.** S3Dock strips accidental spaces and line breaks from the endpoint, bucket, access key ID, and secret key, but double-check values copied from your provider dashboard.
- **Verify the bucket exists and the keys are correct.** The access key ID and secret key must have permission to list and read (and write, if you upload) the bucket.

## Path-style URL required

Some providers do not support virtual-host bucket addresses. Enable **Use path-style URLs** in the advanced connection settings when connecting to:

- Cloudflare R2
- MinIO
- Ceph
- Self-hosted or custom object storage endpoints

Amazon S3 and most public clouds use virtual-host style and should leave this off.

## Region is required (or must be left blank)

- Most regional providers (Amazon S3, Wasabi, Backblaze B2, DigitalOcean Spaces, Google Cloud Storage) require a **Region**. Use the exact value shown by your provider.
- Some providers (for example certain MinIO or R2 configurations) do not need a region. When left blank, S3Dock still uses `us-east-1` internally for request signing. The connection editor shows "Region (optional)" for those presets.

## "Access Denied" or empty folder

- Confirm the bucket policy or IAM user allows `s3:ListBucket` and `s3:GetObject` for the prefix you are browsing.
- If you see the bucket but no files, the credentials may only have access to a sub-prefix. Navigate to the allowed prefix or adjust the policy.

## Playback or preview does not load

- S3Dock generates **short-lived signed URLs** for images, videos, and audio. If a URL expires mid-session, refresh the folder or reopen the file.
- Video seek may show **Range OK** or **Range fallback**. If seeking stutters, the provider may not support HTTP Range requests; keep **Range check** enabled so the app detects this.
- Increase the **Signed URL hours** (Settings > Network / Object Storage) if large files time out before finishing.

## Signed URLs and sharing

- Signed preview and playback URLs expire after the configured lifetime (1–24 hours). They are not permanent public links.
- When you choose **Open with**, S3Dock shares a short-lived signed URL with the selected app. Enable **Confirm external app open** to be warned before sharing.

## Offline downloads never finish

- Keep Offline uses Wi-Fi-only constraints by default. Connect to Wi-Fi, or disable **Download only on Wi-Fi** in Settings > Offline & Downloads.
- Check that the Android "Downloads" permission is granted on older devices if saving to public Downloads fails.

## Cache grows large

Open Settings > Cache to see usage and raise or lower the per-type limits, or clear images, thumbnails, video stream, or all cache from Maintenance.

## Moving providers

You can switch providers by editing the connection settings instead of changing your whole workflow. Use Settings import/export or a database backup when moving to a new device.
