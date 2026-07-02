---
title: "使い方"
description: "S3Dock の初期設定と基本的な使い方。"
toc: true
---

このページでは、S3Dock の初期設定と基本的な使い方を説明します。スクリーンショットは Android の通知欄とナビゲーションバーを除いた状態で撮影しています。

## 事前に用意するもの

S3Dock はストレージアカウント自体を提供しません。先に利用するオブジェクトストレージのバケットと認証情報を用意してください。

通常は以下が必要です。

- エンドポイント URL
- バケット名
- アクセスキー ID
- シークレットキー
- リージョン（必要なプロバイダーのみ）
- Path-style URL 設定（必要なプロバイダーのみ）

Cloudflare R2、MinIO、Wasabi、Backblaze B2、DigitalOcean Spaces、Amazon S3 など、多くの S3 互換プロバイダーはプリセットから開始して値を編集できます。

## 初回起動

ストレージ接続がまだ設定されていない場合、S3Dock は簡易セットアップ画面を表示します。

<figure class="s3dock-phone-shot">
  <img src="/usage/initial-setup.png" alt="S3Dock の初回セットアップ画面">
  <figcaption>新しく接続を作る場合は Add storage、別端末から移行する場合は Restore backup を使います。</figcaption>
</figure>

選べる操作は次の2つです。

- **Add storage**: Storage 設定を開き、新しいプロバイダーまたはバケットを追加します。
- **Restore backup**: S3Dock で作成したアプリ DB バックアップを復元します。

## ストレージ接続を追加する

初回画面で **Add storage** を押すと、Settings > Storage が開きます。

<figure class="s3dock-phone-shot">
  <img src="/usage/storage-overview.png" alt="S3Dock の Storage 設定概要">
  <figcaption>Storage 画面では、接続状態、保存済みプロバイダー、保存済みバケット、キャッシュ、スキャンフォルダの状態を確認できます。</figcaption>
</figure>

新規インストール直後は、保存済みプロバイダーやバケットがない状態です。

## プロバイダープリセットを選ぶ

**Connection editor** までスクロールし、プロバイダープリセットを選びます。候補が多い場合は検索できます。

<figure class="s3dock-phone-shot">
  <img src="/usage/provider-presets.png" alt="S3Dock のプロバイダープリセット一覧">
  <figcaption>Cloudflare R2、Amazon S3、MinIO、Wasabi、Backblaze B2、DigitalOcean Spaces、Custom Object Storage Provider などを選べます。</figcaption>
</figure>

一覧にない S3 互換プロバイダーを使う場合は、**Custom Object Storage Provider** を選んでください。

## 接続情報を入力する

プリセットを選んだら、接続情報を入力します。

1. エンドポイントを入力します。
2. バケット名を入力します。
3. アクセスキー ID を入力します。
4. シークレットキーを入力します。
5. 必要な場合だけリージョンを設定します。
6. 必要な場合だけ Path-style URL を有効にします。
7. **Save and Connect** を押します。

S3Dock は接続項目に紛れ込んだ空白や改行を取り除きますが、プロバイダーの管理画面からコピーする時は値を慎重に確認してください。

## バックアップから復元する

別端末などで S3Dock のアプリ DB バックアップを作成済みの場合は、初回画面の **Restore backup** を使います。

DB バックアップはアプリ移行用です。平文バックアップを選択した場合、別端末でも復元できるように接続情報が平文で含まれます。バックアップファイルは安全に管理し、不要になったら削除してください。

## ファイルを閲覧する

接続に成功すると、**Files** タブで現在のバケットフォルダを表示できます。

主な操作:

- 検索で現在のフォルダ内を絞り込む
- 表示ボタンでリスト、グリッド、Masonry を切り替える
- 並び替えで名前、更新日時、サイズ順を切り替える
- フォルダをタップして移動する
- 画像、動画、音楽をタップしてメディアビューアで開く
- プラスボタンからファイルアップロード、フォルダアップロード、フォルダ作成、カメラ取り込みを行う

## メディアライブラリ

Photos、Videos、Music、Documents は、指定したバケットフォルダをスキャン対象にできます。スキャンフォルダが未設定の場合は、各タブを開いて対象フォルダを選んでください。

Music では、メタデータが取得できる場合に曲、アーティスト、アルバム、フォルダで閲覧するスマートライブラリも利用できます。

## オフライン保持とキャッシュ

ファイルメニューの **Keep Offline** を使うと、ファイルを端末に保存して後から利用できます。保存済みファイルは Offline タブに表示されます。キャッシュ上限や削除は Settings から管理できます。

## セキュリティ上の注意

- HTTPS エンドポイントの利用を推奨します。
- HTTP エンドポイントは信頼できるローカルネットワークでのみ利用してください。
- 外部アプリで開く場合、短時間だけ有効な署名付き URL が外部アプリに渡されます。
- 認証情報を含むバックアップファイルは共有しないでください。
