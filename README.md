# 刈谷市 学校マップ（追加しやすいWeb版）

## ファイル構成

- `index.html`：地図の表示・検索・絞り込みなどのプログラム
- `schools.js`：学校情報だけをまとめたデータファイル
- `README.md`：この説明書

## 学校を追加する方法

`schools.js` を開いて、`const schools = [` の中に学校を1件追加します。

例：

```javascript
{
  name: "○○中学校",
  type: "中学校",
  town: "○○町",
  address: "愛知県刈谷市○○町1-1",
  deviation: null,
  elementaryDistrict: "○○小学校",
  juniorHighDistrict: "○○中学校",
  schoolStyle: "○○な校風",
  access: "○○駅から徒歩○分"
},
```

### `type` に入れる値

- `小学校`
- `中学校`
- `高校`

学校の色分けや検索・絞り込みは、`type` をもとに自動で行われます。

### 偏差値

偏差値がない学校は、

```javascript
deviation: null,
```

とします。

偏差値がある高校なら、

```javascript
deviation: 68,
```

のように数字を入れます。

## 今後追加できる情報

`schools.js` に項目を追加して、地図側の表示を拡張できます。

例：

```javascript
schoolStyle: "自由な校風",
access: "刈谷駅から徒歩10分",
university: "国公立大学への進学実績あり",
club: "運動部が盛ん",
uniform: "制服あり"
```

## Web公開

このフォルダの `index.html` がトップページになります。

GitHub Pagesなどの静的Webホスティングに、この3ファイルをアップロードすれば公開できます。

## 注意

現在の地図は、地図タイル・住所検索・町境データなど一部の外部Webサービスをブラウザから利用します。
そのため、公開後もインターネット接続が必要です。

また、学校情報・学区・偏差値などは変更される場合があるため、公開前に最新情報を確認してください。
