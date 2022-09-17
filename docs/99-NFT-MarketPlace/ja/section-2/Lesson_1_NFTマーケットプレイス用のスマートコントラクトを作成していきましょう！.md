### 👩‍💻 Bunzz を使用したコントラクトの作成

ここでは、Bunzz を使ってスマートコントラクトを作成していきます。

Bunzz は dApp を構築するスマートコントラクトをモジュールとして簡単に利用できる開発プラットフォームです。

dApp 開発に必要な主要コントラクトやコンパイル、セキュリティ監査済のスマートコントラクトを予め利用できる環境をエンジニア向けに提供しています。


**Bunzz で行うこと**

1.  Create Dappでスマートコントラクトを作成
2.  各項目を入力する
3.  アプリケーションのData API root URLを設定

まずは、Metamask を Bunzz に接続します。

今回は `Goerli Testnet` を利用するので、接続した際には Metamask のネットワークが `Goerli Testnet` になっていることを必ず確認しておいてください。

※ Goerli ETH をお持ちでない場合は[こちら](https://goerlifaucet.com/)の faucet から取得してください。
![](/public/images/99-NFT-MarketPlace/section-2/2_1_1.png)

続いて、こちらから [Bunzz](https://app.bunzz.dev/) の画面に進み、「Create Dapp」をクリックしてDappを作成します。

![](/public/images/99-NFT-MarketPlace/section-2/2_1_2.png)

好きな Dapp Name を入力して `Create` ボタンをクリックします。
![](/public/images/99-NFT-MarketPlace/section-2/2_1_3.png)

Network Name を選択して、`Next` ボタンをクリックします。（今回は `Goerli Testnet` を利用しています。）
![](/public/images/99-NFT-MarketPlace/section-2/2_1_4.png)

続いて、`Simple NFT MarketPlace` を選択します。
![](/public/images/99-NFT-MarketPlace/section-2/2_1_5.png)

ここで一度 Bubble の画面に戻り、`Settings` タブの中にある `API` タブから `Data API root URL` を取得します。
![](/public/images/99-NFT-MarketPlace/section-2/2_1_6.png)

続いて、Bunzz に戻り、以下の情報設定を行います。
![](/public/images/99-NFT-MarketPlace/section-2/2_1_7.png)

* name（好きなトークン名を入力）
* symbol（好きなシンボル名を入力）
* baseTokenURI（先ほど取得したData API root URLをペーストし、以下のように変更してください。）
  1. `obj` を削除 
   https://test-nft0011.bubbleapps.io/version-test/api/1.1/ ~~obj~~
  2. `contents` を記載
    [https://test-nft0011.bubbleapps.io/version-test/api/1.1/contents/](https://test-nft0011.bubbleapps.io/version-test/api/1.1/contents/)

※ Bubble の Data API は有料プランから使える機能です。

デプロイするためにはガス代がかかりますので、Metamask の画面が表示されたら適宜 `確認` ボタンを押しましょう。
![](/public/images/99-NFT-MarketPlace/section-2/2_1_8.png)

以下の画面が表示されたらコントラクトの生成は完了となります。
![](/public/images/99-NFT-MarketPlace/section-2/2_1_9.png)


### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `Bunzz-marketplace` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 4 点を記載してください ✨

```
1. 質問が関連しているセクション番号とレッスン番号
2. 何をしようとしていたか
3. エラー文をコピー&ペースト
4. エラー画面のスクリーンショット
```

---

おめでとうございます！　セクション 2 が終了しました 🚀

デプロイが完了した画面を `Bunzz-marketplace` に投稿して、あなたの成功をコミュニティで祝いましょう 🎉

次のセクションに進みましょう！
