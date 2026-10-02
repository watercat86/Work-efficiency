# Work-efficiency

<p align="center">
  <strong>自分用のHTMLツール箱</strong><br>
  HTMLを書く作業をラクにするための、いろいろなWebエディタをぶっこみました。
</p>

## 🌐 オンラインで使う

**GitHub Pages で公開中！**

👉 https://watercat86.github.io/Work-efficiency/

ブラウザで開くだけで、すぐに使えます。

## 🎮 ツール

### Parts Rig Editor
**キャラクターのスプライトを図形で組み立てるエディタ**

👉 https://watercat86.github.io/Work-efficiency/parts-rig-editor/

- 四角形・円・三角形・多角形などの図形でキャラクターを設計
- 関節(基準点)を設定して、親子関係で骨組みを作成
- AIに「右腕を振るコード」を頼めるようにJSON書き出し対応
- ゲーム用のスタンドアロンHTMLも自動生成

**使い方：** キャンバスに図形を置く → 親子関係を作る → roleを付けて意味を設定 → JSONを書き出してAIに渡す

---

### Sonic Forge
**ビジュアル編集でゲーム音・BGMを作成するDAW**

👉 https://watercat86.github.io/Work-efficiency/sonic-forge/

- 複数のトラック(wave形状, ノイズなど)で音を重ねられる
- ピアノロール風UIでノートを置いて作曲
- リアルタイムプレイバック＋ループ再生対応
- WAVファイルに書き出し可能

**使い方：** トラックを選ぶ → ノートを置く → 再生して確認 → WAV書き出し

---

## 📦 ファイル構成

```
Work-efficiency/
├── index.html                    # ポータルサイト（玄関）
├── parts-rig-editor/
│   └── index.html               # Parts Rig Editor
├── sonic-forge/
│   └── index.html               # Sonic Forge
├── _config.yml                   # GitHub Pages設定
├── .github/
│   └── workflows/
│       └── deploy.yml           # 自動デプロイワークフロー
└── README.md                     # このファイル
```

## 🚀 始め方

### ローカルで開く
```bash
# このリポジトリをクローン
git clone https://github.com/watercat86/Work-efficiency.git

# フォルダを開く
cd Work-efficiency

# index.html をブラウザで開く
# (例: ドラッグ＆ドロップ、またはダブルクリック)
```

### サーバーで開く（推奨）
```bash
# Python 3
python -m http.server 8000

# または Node.js
npx http-server
```
その後、ブラウザで `http://localhost:8000` を開く

## 💡 使用例

### Parts Rig Editor
```
1. 「＋四角形を追加」で胴体を作成
2. 胴体を選んだ状態で「＋四角形を追加」で腕を追加(子パーツになる)
3. 腕の「基準点」を肩の位置にドラッグ
4. 腕の「role」に「arm_r」と入力
5. 「JSONを書き出す」でAIに渡す
   → AIが「振る」「曲げる」などのコードを生成
```

### Sonic Forge
```
1. 上部で楽器(waveform)を選ぶ
2. ペン🖊️ツールに切り替え
3. ピアノロール(中央)をドラッグしてノートを描く
4. 「Play▶」で再生確認
5. 気に入ったら「Export WAV」で保存
```

## 🛠️ 技術スタック

- **言語:** HTML + CSS + JavaScript
- **ホスティング:** GitHub Pages
- **CI/CD:** GitHub Actions

## ✨ 機能一覧

### Parts Rig Editor
- ✅ 図形描画(四角・円・三角形・多角形・星・半円・円弧・自由形)
- ✅ グループ化(見えない親パーツで関節を作成)
- ✅ 親子付け替え(ドラッグで階層変更)
- ✅ 基準点編集(回転・スケールの軸を設定)
- ✅ 頂点編集(三角形・自由形の頂点を直接変更)
- ✅ JSON書き出し＆読み込み
- ✅ ゲーム用HTMLスタンドアロン生成
- ✅ ポーズ確認(役割を持つパーツを動かしてテスト)
- ✅ ズーム＆パン操作
- ✅ Undo/Redo

### Sonic Forge
- ✅ 複数トラック(最大8色の音色)
- ✅ Wave形状選択(sine, square, sawtooth, triangle, noise)
- ✅ ピアノロール式の作曲
- ✅ BPM変更
- ✅ ループ再生＆スナップ機能
- ✅ ノート削除・長さ変更
- ✅ トラック/ノート個別制御(ボリューム、ミュート、ソロ)
- ✅ SEプリセット(Coin, Jump, Laser, Power Up, Hit, Explosionなど)
- ✅ WAV書き出し
- ✅ JSON保存＆読み込み(シーケンス再利用)
- ✅ Attack/Release設定(音声エンベロープ)

## 🎯 今後やりたいこと

- [x] オンライン公開(GitHub Pages)
- [ ] Parts Rigger: ゲーム用ランタイムの充実
- [ ] Sonic Forge: MIDIファイル読み込み
- [ ] 複数のサンプルキャラ・BGM集
- [ ] AI連携ガイド

## 📄 ライセンス

自分用なので自由に使ってください。

## 👤 作者

**watercat86**  
- GitHub: [@watercat86](https://github.com/watercat86)

---

**質問・バグ報告など、Issueでお知らせください。** 🐛
