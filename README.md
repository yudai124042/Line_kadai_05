# Line_kadai_05
ライン風のアプリの課題。firebase使用。
# 🗨️ 匿名お悩み相談箱

---

## ① 課題名  
Firebase Realtime Database を活用した、匿名相談・返信・いいね機能付きリアルタイムチャットアプリ

---

## ② 課題内容（どんな作品か）  
ユーザーが匿名で悩みを投稿でき、他のユーザーから返信をもらえるシンプルなチャットアプリです。  
また、投稿に対して「❤️ いいね」ボタンを押して共感を示すこともできる設計になっており、**リアルタイムで投稿が反映・更新されるUI**をFirebaseだけで実現しています。

---

## ⑤ 工夫した点・こだわった点  

- 🔁 **Firebase Realtime Databaseによるリアルタイム表示**  
  投稿・返信・いいねの更新がリアルタイムで反映されるように設計。
  
- ❤️ **いいね数のリアルタイム反映**  
  すべての投稿に「いいね（共感）」ボタンを実装し、押すたびにカウントアップ。
  
- 🎨 **CSSの統一感とやさしい配色**  
  オレンジ×白を基調に、誰でも使いやすい安心感のあるデザインを心がけた。
  
- 📱 **スマホでも見やすいレイアウト**  
  モバイル画面でも快適に投稿・閲覧できるよう、フォームとUIを最適化。

---

## ⑥ 難しかった点・次回トライしたいこと  

- ❗ `onValue()` を使った「いいね数のリアルタイム更新」の記述場所に苦戦  
  → `postId` のスコープ問題を理解して、`onChildAdded` の中に正しく配置することで解決。

- 🔜 **次回トライしたい機能**  
  - 1人1回までのいいね制限（IP記録 or 匿名認証を使う）
  - 投稿の並び替え（いいね順、新着順など）
  - 通報・削除機能（モデレーション対策）
  - 返信に「いいね」やスタンプなどリアクション機能
