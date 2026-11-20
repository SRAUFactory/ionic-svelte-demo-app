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
- **ネイティブ開発環境 (エミュレータ・実機デバッグ時)**:
  - **iOSデバッグ**: Xcode (macOS環境)
  - **Androidデバッグ**: Android Studio

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

#### 方法 A: VS Code / Antigravity IDE 拡張機能の利用（推奨）

VS Code や Antigravity IDE をお使いの場合は、Ionic公式の **Ionic (Web Native)** 拡張機能の利用を推奨します。

1. 拡張機能マーケットプレイスで `Web Native` または `Ionic` を検索してインストールします。
2. サイドバーのアクティビティバーに追加された Ionic アイコンを開きます。
3. **Run** / **Debug** セクションからターゲット（iOS Simulator, Android Emulator, 実機等）を選択し、ワンクリックでビルドおよびデバッグ起動が可能です。

#### 方法 B: CLI ＋ Xcode / Android Studio を使う方法

Capacitor CLI を経由してネイティブIDEを起動してデバッグを行う標準手順です。

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
