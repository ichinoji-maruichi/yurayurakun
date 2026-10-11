# ゆらゆらくん

イラストをアップすると、AIが奥行きを読み取って立体的に揺れるアニメにする、単一HTMLのブラウザアプリ。画像はブラウザの中だけで処理される。

## 機能

- AIによる奥行き推定（Depth Anything V2 small、初回のみ約30MBのモデルを読み込み）。使えない時は明るさから奥行きを作成
- 動き：往復 / 2コマ / ぐるっと。揺れる方向はダイヤルで指定
- 揺らす所をなぞる（マスク）・手前にする / 奥にする（奥行きの手修正）・元に戻す
- ピント合わせ、背景カット、奥行きのカーブ、なめらかさ、輪郭の補正、背景ぼかし
- 保存：GIF / APNG / 動画（MP4、非対応ブラウザはWebM）、奥行き画像（PNG）
- 使い方ヘルプ（? ボタン）

## 使い方

`index.html` をブラウザで開くだけ。ビルド不要（WebGL必須）。

## 使用ライブラリ（CDN）

- [@huggingface/transformers](https://github.com/huggingface/transformers.js) 3.5.1（jsDelivr）— Apache-2.0
- [gifenc](https://github.com/mattdesl/gifenc) 1.0.3（jsDelivr）— MIT
- モデル: onnx-community/depth-anything-v2-small（フォールバック: Xenova/depth-anything-small-hf）
