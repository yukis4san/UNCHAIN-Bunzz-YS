### 👩‍💻 **Mint,List,Buyを各画面で実装**

ここでは、各画面ごとにBunzzSDKを通じて、Mint,List,Buy等のFunctionを呼び出していきます。

**実装する画面**

*   NFTコンテンツ作成ページ

このページでは、NFTのMINTを行います。
BunzzSDKを通じて、mint関数を呼び出していきます。
この画面は実装がされていますが、重要な内容になりますので、一通り確認いただきながらレッスンを進めてください。


**Workflow画面へ移動します**

まずは、Bubbleない画面のWorkflow画面へ遷移しましょう。
「Create」ボタンがクリックされたときに、NFTを新たに作成・発行を行いますが、その際にBunzzの「Update action」を通じて、mintを行っています。
画面左側に縦に並んでいるタブの上から2つ目にある「Workflow」を選択してください。


### **NFTコンテンツ作成ページ**

Workflow画面には、「When」と書かれている正方形のボックスが並んでいますので、「Button Create is clicked」と書かれているボックスをクリックしてください。
クリックすると、正方形のボックス下部に「Step1」などの長方形のボックスが出てくるので、「Step3」の「Update Action BunzzSDK A」を選択してください。
すると黒色のpropertyが立ち上がります。
確認して次のステップへ進んでください。

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FOn-bUrPRh.png?alt=media)

次に「Module Name」　と「Function Name」を設定してmint関数を呼び出す準備をしていきます。
- 「Module Name」に「NFT(ERC721)」を入力します（今回は入力されています）
- 「Function Name」に「mint」を入力します（今回は入力されています）

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FEtvfC9So6.png?alt=media)

最後に「argument」に「address」と「tokenId」を設定していきます。
- 「address」にSetup時に取得している「Signer Address」を設定します
- 「tokenId」にコンテンツの「id」を設定します
※この際にBubbleでレコード生成時に自動で生成されるuniqueIdを利用しないよう注意してください

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FMdAYoddDP.png?alt=media)

これでNFTを新たに作成できるようになりました。



### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `#section-1` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 3 点を記載してください ✨

    1. 質問が関連しているセクション番号とレッスン番号
    2. 何をしようとしていたか
    3. エラー文をコピー&ペースト
    4. エラー画面のスクリーンショット


* * *

環境設定が完了したら、次のレッスンに進んでください 🎉
