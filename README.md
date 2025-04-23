# GoogleVisionOCR

高品質OCRアプリケーション - ScanSnapとKindleファイルの変換ツール

## 概要

GoogleVisionOCRは、スキャンされたPDFやKindleのEPUBファイルからテキストを抽出し、
検索可能な形式に変換するデスクトップアプリケーションです。Google Cloud Vision APIを
使用して高精度なOCR処理を行い、日本語の縦書きテキストにも対応しています。

## 機能

- ScanSnapから取り込んだPDFの高品質OCR処理
- KindleのEPUBファイルからのテキスト抽出
- 画質を維持したままのOCR処理
- 縦書きテキスト対応
- モダンなUI/UXデザイン

## 技術スタック

- GUI: Qt6 (PyQt6)
- OCRエンジン: Google Cloud Vision API
- 開発言語: Python
- パッケージ管理: PIP / venv

## インストール

```bash
# 仮想環境を作成
python -m venv .venv
# 仮想環境を有効化
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

# 依存パッケージをインストール
pip install -r requirements.txt
```

## 使用方法

```bash
python -m src.main
```

## プロジェクト構造

```
GoogleVisionOCR/
├── src/
│   ├── main.py               # アプリケーションエントリポイント
│   ├── core/
│   │   ├── ocr_engine.py     # OCR処理コア機能
│   │   ├── pdf_handler.py    # PDF処理モジュール
│   │   ├── epub_handler.py   # EPUB処理モジュール
│   │   └── image_processor.py # 画像前処理
│   ├── ui/
│   │   ├── main_window.py    # メインウィンドウ
│   │   ├── preview_panel.py  # プレビューパネル
│   │   ├── settings_dialog.py # 設定ダイアログ
│   │   └── resources/        # アイコン等のリソース
│   └── utils/
│       ├── config.py         # 設定管理
│       ├── file_manager.py   # ファイル入出力
│       └── logger.py         # ログ管理
├── tests/                    # テストコード
├── requirements.txt          # 依存パッケージリスト
└── setup.py                  # セットアップスクリプト
```

## ライセンス

このプロジェクトはMITライセンスの下で提供されています。
