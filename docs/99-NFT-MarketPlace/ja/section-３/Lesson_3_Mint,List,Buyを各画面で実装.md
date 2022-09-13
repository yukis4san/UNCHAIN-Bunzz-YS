### 👩‍💻 **Mint,List,Buyを各画面で実装**

ここでは、各画面ごとでMint,List,BuyのFunctionを呼び出す実装を行なっていきます。

**実装する画面**

*   NFTコンテンツページ
こちらのページでは、Marketplaceへ「List」されているアイテムを購入「buy」する工程を実装して行きます。
BunzzSDKを通じて、「buy」関数を呼び出して行きます。


**Workflow画面へ移動します**

まずは、Bubbleない画面のWorkflow画面へ遷移しましょう。
画面左側に縦に並んでいるタブの上から2つ目にある「Workflow」を選択してください。


### **NFTコンテンツページ**

最後にマーケットプレイスからNFTコンテンツを購入する方法をご紹介します


まず、「BUY NOW」ボタンがクリックされたときに、NFTコンテンツの購入を行いますが、その際にBunzzの「Update action」を設定します

Workflow画面には、「When」と書かれている正方形のボックスが並んでいますので、「Button BUY NOW is clicked」と書かれているボックスをクリックしてください。
クリックすると、正方形のボックス下部に「Step1」などの長方形のボックスが出てくるので、「Step1」の「Update Action BunzzSDK A」を選択してください。
すると黒色のpropertyが立ち上がります。
確認して次のステップへ進んでください。

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FPSeDj_lnX.png?alt=media)


次に「Module Name」　と「Function Name」を設定してbuy関数を呼び出す準備をしていきます。
- 「Module Name」に「Simple Marketplace (For NFT)」を入力します（今回は入力されています）
- 「Function Name」に「buy」を入力します（今回は入力されています）

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FJgeaMrQpU.png?alt=media)

最後に「tokenId」に「id」、「value」にコンテンツの「price」をnumberに変換して設定ます

最後に「argument」に「tokenId」と「value」を設定していきます。
- 「tokenId」にコンテンツの「id」を設定します
- 「price」にコンテンツの「price」をnumber型に変換して設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FZ_I_7EWdi.png?alt=media)

これでマーケットプレイスからの「購入」の実装ができました！



### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `#section-3` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 3 点を記載してください ✨

    1. 質問が関連しているセクション番号とレッスン番号
    2. 何をしようとしていたか
    3. エラー文をコピー&ペースト
    4. エラー画面のスクリーンショット
    

* * *

環境設定が完了したら、次のレッスンに進んでください 🎉
