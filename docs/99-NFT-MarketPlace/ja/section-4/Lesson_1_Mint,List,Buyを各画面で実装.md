### 👩‍💻 **Mint,List,Buyを各画面で実装**

ここでは、各画面ごとにBunzzSDKを通じて、Mint,List,Buy等のFunctionを呼び出していきます。

**実装する画面**

*   NFTコンテンツ作成ページ


### **NFTコンテンツ作成ページ**

「Create」ボタンがクリックされたときに、NFTを新たに作成・発行を行いますが、その際にBunzzの「Update action」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FOn-bUrPRh.png?alt=media)

次に「Module Name」に「NFT(ERC721)」、「Function Name」に「mint」を入力します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FEtvfC9So6.png?alt=media)

最後に「address」にSetup時に取得している「Signer Address」、「tokenId」にコンテンツの「id」を設定して完了です（この際にBubbleで生成されるuniqueIdを利用しないよう注意してください）

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FMdAYoddDP.png?alt=media)

これでNFTを新たに作成できました！



### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `#section-1` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 3 点を記載してください ✨

    1. 質問が関連しているセクション番号とレッスン番号
    2. 何をしようとしていたか
    3. エラー文をコピー&ペースト
    4. エラー画面のスクリーンショット
    

* * *

環境設定が完了したら、次のレッスンに進んでください 🎉
