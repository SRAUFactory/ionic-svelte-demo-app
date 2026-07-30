# ionic-svelte-demo-app

このプロジェクトは、**Ionic Framework**、**Svelte (SvelteKit)**、そして **Capacitor** を組み合わせたモバイルアプリ開発のデモアプリケーションです。

## 概要

Webフロントエンド技術 (HTML/CSS/JS) とSvelteのリアクティビティを活かしつつ、IonicのUIコンポーネント群を用いてiOS/Androidネイティブライクな見た目と動きを実現しています。

詳細は、以下の記事もご参照ください。
- [Ionic + Svelteにおける役割分担と、Flutter/ネイティブ開発との決定的な違い](https://qiita.com/SRAUFactory/)
- [IonicとSvelteでのアプリのプロジェクト追加 (pnpm対応版)](https://qiita.com/SRAUFactory/)

## 前提条件

- **Node.js**: 最新のLTS推奨
- **パッケージマネージャー**: `pnpm` を必ず使用してください (モジュール解決のエラーを防ぐため、プロジェクトルートの `.npmrc` に `shamefully-hoist=true` が設定されています)

## 環境構築・起動手順

### 1. 依存関係のインストール

```bash
pnpm install
```

### 2. ローカルサーバー（ブラウザ）での確認

```bash
pnpm dev
```
起動後、ブラウザから `http://localhost:5173` 等にアクセスして表示を確認できます。

### 3. iOS / Android エミュレータでのデバッグ

Capacitorを経由してネイティブ環境でデバッグを行う場合は、各種IDE（Xcode / Android Studio）を利用するのが正攻法です。

```bash
# 事前にWebアセットのビルドを実施
pnpm build

# iOSの場合: プロジェクトの同期とXcodeの起動
pnpm cap sync ios
pnpm cap open ios

# Androidの場合: プロジェクトの同期とAndroid Studioの起動
pnpm cap sync android
pnpm cap open android
```
それぞれのIDEが起動したら、ターゲットとなるデバイス（シミュレータ / エミュレータ）を選択し、Run（実行）ボタンからアプリを起動してください。
※ `pnpm dev :ios` や `pnpm dev :android` などのコマンドは直接動作しませんのでご注意ください。
