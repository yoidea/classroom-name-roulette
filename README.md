# 指名ルーレット

授業で生徒を指名するためのブラウザ用ルーレットです。

## 使い方

`index.html` をブラウザで開きます。

1. 画面右下の `設定` を開き、候補の名前を追加します。画像や色、抽選モードもここで設定できます。

   <img src="docs/screenshots/settings.jpg" alt="候補管理画面" width="520">

2. `スタート` ボタンまたはスペースキーでルーレットを開始し、`ストップ` ボタンまたはEnterキーで停止します。

   <img src="docs/screenshots/roulette.jpg" alt="ルーレット画面" width="520">

3. 画面右下の `集計` から、指名された回数を確認できます。

   <img src="docs/screenshots/stats.jpg" alt="集計画面" width="520">

## 主な機能

- 候補名、画像、色の登録
- 完全ランダム / 平等に当てるモードの切り替え
- 欠席者の一時除外
- 指名回数の集計
- JSONによる候補データの書き出し/読み込み
- `se/` 配下の効果音再生

## 保存データ

ブラウザの `localStorage` には、候補一覧、直近結果、抽選モード、指名回数、欠席状態が保存されます。

JSON書き出しには候補マスタだけを含めます。

- `name`
- `image`
- `color`

`hitCount`、`absent`、`textColor`、直近結果、抽選モードはJSONには含めません。

## 効果音

効果音ファイルは `se/` ディレクトリに配置します。HTMLから相対パスで参照しています。

- `start.mp3`: 開始時
- `spin-loop.mp3`: 回転中
- `slow-down.mp3`: 減速中
- `result.mp3`: 結果表示時

効果音素材: [効果音ラボ](https://soundeffect-lab.info/)

効果音ラボの利用規約では、報告・リンク・クレジット表記は任意です。
