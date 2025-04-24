# LINE × ChatGPT Bot

LINEメッセージを受け取って、OpenAI API (gpt-3.5-turbo) で自動応答するLINE Botです。

## 概要
- LINE DevelopersでBot作成
- FlaskサーバーでWebhook受信
- OpenAI APIと連携してメッセージ生成
- `.env`ファイルによる安全なキー管理
- `ngrok`でローカルサーバーに外部アクセスを通す

## 使用技術
- Python 3.11+
- Flask
- line-bot-sdk
- openai
- ngrok

## 構成ファイル

- `app.py` - メインのFlaskアプリ
- `.env.example` - 必要な環境変数のテンプレート
- `requirements.txt` - 依存ライブラリ一覧

## ローカルでの起動方法

```bash
# 仮想環境推奨
python -m venv venv
source venv/bin/activate  # Windowsなら venv\Scripts\activate

# ライブラリをインストール
pip install -r requirements.txt

# .env を用意（example をコピーして中身を記入）
cp .env.example .env

# Flaskアプリ起動
python app.py
