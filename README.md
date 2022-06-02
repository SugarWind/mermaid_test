# 課題
Mermaidを触ってみよう

マークダウンファイルを編集して、Mermaidで図を描いてみよう

# 取り組み方
* 本プロジェクトをforkしてください。
* README.mdを編集して、Mermaidを使いこなしてください
* できたらプルリクエストを出します

# 課題項目
## 流れ図
### 条件
- 開始と終了ノードをつける
- 条件分岐を組み込む
- 5ノード以上
- カッコいいほど高得点

## 解答
```mermaid
flowchart LR;
  A(["開始"]) --> B["正解を乱数で決定"];
  B --> C[/"値を入力"/]
  C --> D{"正解＝＝入力した値"}
  D --　真 --> E[/"正解と表示"/];
  D -- 偽--> G{"正解 > 入力した値"}
  G -- 真 --> H[/"入力した値が正解より小さいと表示"/]
  H --> C
  G --偽 --> I[/"入力した値が正解より大きいと表示"/]
  I --> C
  E --> F(["終了"])
```
-数当てゲームをテーマに作成しました。

## シーケンス図
### 条件
- 3人以上
- メッセージをやり取りしない人がいないように
- 自己呼び出しを含むこと
- カッコいいほど高得点

## 解答
```mermaid
sequenceDiagram
 participant ユーザー
 participant 予約画面
 participant サーバー
 ユーザー->> 予約画面:予約日時を入力
 予約画面->> サーバー:予約日時を送信
 loop サーバー
 サーバー->> サーバー:予約日時を記録
 end
 サーバー->>ユーザー:予約番号を発行
```
-映画館の予約をテーマに作成しました。

## クラス図

### 条件
- 3つ以上
- 汎化と集約を含むこと
- カッコいいほど高得点

## 解答
