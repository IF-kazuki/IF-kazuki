---
title: "report app"
repository: "https://github.com/IF-kazuki/report-app"
---

## Report App

Hosting url <https://vercel.com/if-kazuki/report-app/FovSi6kmUNJFFzqXDixJEuwfqYUz>  
repository <https://github.com/IF-kazuki/report-app>

### 何を作ったか

相手の書き込みをリアルタイムで見れる web アプリ

### 作成した経緯

コロナ渦で相手の手元が見えないので、すこしでも生徒の状況がみれるようなアプリがあれば授業が円滑に行えると考えたからです。

### 主な機能

リアルタイムで相手の書き込みを見れる機能。  
提出したデータを保存できる機能。  
提出先に細かな設定を行うことができる。  
簡単に提出ができる機能

### 使用技術

**言語**  
 HTML  
 CSS / CSS modules  
 JavaScript / TypeScript

**フレームワーク**  
 Next.js(React) v12.1.0  
 SSR/API Routes/を使えばバックエンドなしでも session による認証が必要なページを作成できるために採用 fuctions は従量化課金生のプランでしかできないので、できるだけ使用したくなかったという経緯があります。

**ホスティング**  
 Vercel  
 Next.js と親和性が高く簡単にデプロイ、CICD を行ってくれるために採用しました。

**バックエンド**  
Firebase v9

auth  
 データを保存できるように gmail にデータを紐付けれるように使用しました。

firestore  
 提出先のデータを保持するために使用しました。

database  
 テキスト入力をリアルタイムで同期するために使用しました。

storage  
 提出してもらったデータを大量に保存しておくために使用しました。

functions  
 database にデータを大量に保持すると料金がかかるため安価な storage への定期実行のために使用しました。

開発環境  
 ubuntu20.04LTS  
 vscode  
 node.js  
 firebase emulators  
 create-next-app

### その後

没案になったため開発を中断しました。  
理由として自分の類似するサービスの調べが甘かった。開発が楽しくて目をそらしていた。  
Firebase のプランを無料プランに変更したため functions が動かないです。

※未実装機能 functions による storage へのデータ移行の定期実行

### 感想

今回は調べが甘かったのと事前の設計が不十分で二、三回作り直してしまいました。結果 3 週間もかかってしまいました。今後は大した技術選定を行っているわけではないですが、使用技術選びにはしっかり時間をかけます。

### その他

細かい設計などはリポジトリにある document に記載
