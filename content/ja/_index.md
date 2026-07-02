---
title: "S3Dock"
description: "オブジェクトストレージ用 Android クライアント。"
eyebrow: "オブジェクトストレージ用 Android クライアント"
lead: "自分で管理しているオブジェクトストレージのバケットを、Android から実用的なクラウドドライブのように扱えるアプリです。"
primaryAction: "プライバシーポリシー"
toc: true
---

自分で管理しているオブジェクトストレージのバケットを、Android から実用的なクラウドドライブのように扱えるアプリです。

## ユーザー所有のストレージ向け

S3Dock はクラウドアカウントを提供しません。Amazon S3、Cloudflare R2、MinIO、Wasabi、Backblaze B2、DigitalOcean Spaces、その他のバケットエンドポイントをユーザー自身が設定して利用します。

一般的なクラウドドライブの容量プランやアップロード制限、移行しづらさが合わない場合でも、オブジェクトストレージならプロバイダー、バケット、リージョン、料金体系を自分で選べます。

{{< cards >}}
  {{< card title="閲覧と管理" icon="folder" subtitle="リスト、グリッド、Masonry 表示、検索、並び替え、お気に入り、アップロード、ダウンロード、移動、名前変更、削除に対応します。" >}}
  {{< card title="メディアプレビュー" icon="photograph" subtitle="写真、動画、音楽をアプリ内ビューアで開けます。サムネイル、キャッシュ管理、バックグラウンド音楽再生にも対応します。" >}}
  {{< card title="オフライン保持" icon="cloud-download" subtitle="選択したファイルをオフラインで利用できるように保存し、設定画面からローカルキャッシュ容量を管理できます。" >}}
{{< /cards >}}

## デモとスクリーンショット

以下の短いデモでは、S3Dock をオブジェクトストレージバケット用のモバイルファイルマネージャーとして使っている様子を確認できます。

<div class="s3dock-demo-video">
  <iframe src="https://www.youtube.com/embed/WSmvRj0nJXc" title="S3Dock Android app demo" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

<div class="s3dock-screenshot-grid">
  <figure>
    <img src="/showcase/app-files.webp" alt="S3Dock のファイルブラウザでバケット内フォルダを表示している画面">
    <figcaption>検索、並び替え、表示切り替え、ファイル操作を使いながらバケット内フォルダを閲覧できます。</figcaption>
  </figure>
  <figure>
    <img src="/showcase/app-media.webp" alt="S3Dock のグリッド表示とアップロード操作">
    <figcaption>グリッド表示、フォルダプレビュー、展開式アップロード操作を利用できます。</figcaption>
  </figure>
  <figure>
    <img src="/showcase/app-settings.webp" alt="S3Dock の Masonry 写真表示">
    <figcaption>画像が多いフォルダは Masonry 表示で一覧性を高められます。</figcaption>
  </figure>
</div>

## オブジェクトストレージをドライブとして使う理由

クラウドドライブは便利ですが、大量の個人アーカイブ、メディアフォルダ、PC とスマホ間のファイル共有では使いづらくなることがあります。使っていない容量分も固定プランとして支払う必要があったり、大量アップロードが遅かったり、他サービスへの引っ越しが難しくなる場合があります。

オブジェクトストレージを使うと、保存先をアプリや特定サービスから切り離して管理できます。

{{< cards >}}
  {{< card title="プロバイダーを選べる" icon="server" subtitle="R2、MinIO、Wasabi、B2、Spaces、Amazon S3、その他の互換エンドポイントを利用できます。接続設定を変えるだけで、同じ操作感のまま保存先を切り替えられます。" >}}
  {{< card title="Rclone などと併用しやすい" icon="terminal" subtitle="同じバケットを Linux、macOS、Windows から Rclone でマウントや同期し、Android 側では S3Dock をファイルマネージャーとして使えます。" >}}
  {{< card title="リージョンを選べる" icon="globe-alt" subtitle="対応プロバイダーでは近いリージョンや料金面で合うリージョンを選択できます。プレビュー、アップロード、メディア再生の体感にも影響します。" >}}
{{< /cards >}}

<figure class="s3dock-wide-shot">
  <img src="/showcase/r2-usage.webp" alt="Cloudflare R2 の利用状況例">
  <figcaption>Cloudflare R2 などのオブジェクトストレージは、料金、リージョン、リクエスト体系が用途に合う場合、個人アーカイブにも使いやすい選択肢になります。</figcaption>
</figure>

## S3Dock が得意なこと

- 開発者管理のファイルサーバーを経由せず、バケット内のファイルを直接管理
- 写真や動画フォルダのプレビュー
- バケット内の音楽再生とバックグラウンド再生
- 旅行中や通信が不安定な場所でも使いやすいオフライン保持
- 複数プロバイダー、複数バケットの管理
- 端末移行向けの設定エクスポート、DB バックアップ、復元

## 実際の運用を想定した構成

S3Dock は、すでにオブジェクトストレージを使っている人、または自分用の柔軟なクラウドストレージとして使いたい人向けです。バケットのフォルダ構造はそのまま扱いつつ、Photos、Videos、Music、Documents、Favorites、Offline、Transfers、グリッド表示、Masonry 表示、検索、並び替え、フォルダプレビューなど、Android で使いやすい表示を追加しています。

## プライバシーを重視した構成

アプリは Android 端末から、ユーザーが設定したストレージエンドポイントへ直接接続します。S3Dock は、ファイルや認証情報を保存する開発者管理のサーバーを運用しません。

接続情報は端末内に保存され、ユーザーが明示的にバックアップへ含めない限り外部へ出しません。非公開ファイルを外部アプリで開く場合は、短時間だけ有効な署名付き URL を使って、そのファイルだけを一時的に渡します。
