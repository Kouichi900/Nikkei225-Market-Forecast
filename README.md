# Nikkei225-Market-Forecast
日経平均株価（^N225）とNYダウ（^DJI）の過去データを Yahoo Finance から自動取得し、両指数の相関関係を可視化するとともに、線形回帰モデルを用いて翌営業日の日経平均株価を簡易的に予測する Streamlit アプリケーション
[README.md](https://github.com/user-attachments/files/24989757/README.md)
# 日経平均株価予測アプリ

日経平均株価(^N225)とNYダウ(^DJI)の過去データを取得し、相関関係の分析と簡易的なAI予測を行うStreamlitアプリケーションです。

## 機能

- **データ自動取得**: Yahoo Financeから最新の株価データを取得
- **可視化**: 株価推移の比較グラフ、相関図（散布図）の表示
- **AI予測**: 線形回帰分析を用いた、翌営業日の日経平均株価予測

## 必要要件

- Python 3.8 以上
- 以下のPythonライブラリ（`requirements.txt` に記載）:
    - streamlit
    - yfinance
    - pandas
    - numpy
    - scikit-learn
    - plotly
    - statsmodels

## セットアップ手順

1. **リポジトリの準備**:
   ソースコードがあるディレクトリに移動します。

2. **依存ライブラリのインストール**:
   以下のコマンドを実行して必要なライブラリをインストールします。
   ```bash
   pip install -r requirements.txt
   pip install statsmodels
   ```
   ※ `statsmodels` はトレンドライン描画のために追加で必要になる場合があります。

## アプリの起動方法

以下のコマンドを実行すると、ブラウザが立ち上がりアプリが表示されます。

```bash
streamlit run app.py
```

### 起動しない・エラーが出る場合

- **ブラウザが開かない**: ターミナルに表示される `Local URL: http://localhost:8502` をコピーしてブラウザのアドレスバーに貼り付けてください。
- **データ取得エラー**: ネットワーク環境によってはYahoo Financeへの接続が制限されている場合があります。時間を置いて再試行してください。
- **グラフが表示されない**: ブラウザの更新（リロード）を試してください。

## ファイル構成

- `app.py`: アプリケーションのメインファイル
- `data_loader.py`: データ取得・前処理ロジック
- `predictor.py`: 機械学習モデル（予測ロジック）
- `requirements.txt`: 依存ライブラリ一覧

## 画面構成
<img width="2492" height="860" alt="image" src="https://github.com/user-attachments/assets/036c448e-9e62-4fce-a0b0-341930788e00" />
<img width="1886" height="887" alt="image" src="https://github.com/user-attachments/assets/c90bb9f2-6556-4669-9de4-87d6813e20f5" />
<img width="1875" height="1124" alt="image" src="https://github.com/user-attachments/assets/359792a5-4cd6-4ca7-89c3-f5705da911ea" />
<img width="1814" height="1096" alt="image" src="https://github.com/user-attachments/assets/0884b2df-b748-47b4-b51c-d142dc9dfa44" />


