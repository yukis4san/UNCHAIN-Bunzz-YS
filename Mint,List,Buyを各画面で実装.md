### 👩‍💻 **Mint,List,Buyを各画面で実装**

ここでは、各画面ごとでMint,List,BuyのFunctionを呼び出す実装を行なっていきます。

**実装する画面**

*   NFTコンテンツ作成ページ
*   マイNFTコンテンツページ
*   NFTコンテンツページ

### **NFTコンテンツ作成ページ**

「Create」ボタンがクリックされたときに、NFTを新たに作成・発行を行いますが、その際にBunzzの「Update action」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FOn-bUrPRh.png?alt=media)

次に「Module Name」に「NFT(ERC721)」、「Function Name」に「mint」を入力します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FEtvfC9So6.png?alt=media)

最後に「address」にSetup時に取得している「Signer Address」、「tokenId」にコンテンツの「id」を設定して完了です（この際にBubbleで生成されるuniqueIdを利用しないよう注意してください）

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FMdAYoddDP.png?alt=media)

これでNFTを新たに作成できました！

### **マイNFTコンテンツページ**

「NFTコンテンツ作成ページ」で作成されたNFTはまだマーケットプレイスに公開されていないため、NFTマーケットプレイスに公開していきますが、マーケットプレイスへの公開にあたり「承認」と「公開」の2つの手順が必要となるため、本ページでは2つのBunzzSDKを配置します

#### **マーケットプレイスへの承認**

まず、「Publish」ボタンがクリックされたときにマーケットプレイスへの「承認」を行いますが、先ほど同様Bunzzの「Update action」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FlrCdwhM62.png?alt=media)

次に「Module Name」に「NFT(ERC721)」、「Function Name」に「approve」を入力します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FBaNtKPy1h.png?alt=media)

ここで一度Bunzzの「Dashboard」に戻り、マーケットプレイスのaddressを取得します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FY2oZDcU8W.png?alt=media)

Bubbleの画面に戻り、「to」にBunzzで取得したマーケットプレイスの「address」、「tokenId」にコンテンツの「id」を設定して完了です

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FcPy2euIkt.png?alt=media)

これでマーケットプレイスへの「承認」の実装ができましたので、次に「公開」の実装を行っていきます

#### **マーケットプレイスへの公開**

「承認」で利用したBunzzSDKの「Complete Update Action」のEventを設定し、そのactionに2つ目のBunzzSDKの「Update Action」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2F2wh9wlBe0.png?alt=media)

次に「Module Name」に「Simple Marketplace (For NFT)」、「Function Name」に「list」を入力します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FbrewDNnWM.png?alt=media)

最後に「tokenId」に「id」、「price」にコンテンツの「price」をnumberに変換して設定ます

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FvLnT54Pm8.png?alt=media)

これでマーケットプレイスに公開されました！

### **NFTコンテンツページ**

最後にマーケットプレイスからNFTコンテンツを購入する方法をご紹介します

「BUY NOW」ボタンがクリックされたときに、NFTコンテンツの購入を行いますが、その際にBunzzの「Update action」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FPSeDj_lnX.png?alt=media)

次に「Module Name」に「Simple Marketplace (For NFT)」、「Function Name」に「buy」を入力します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FJgeaMrQpU.png?alt=media)

最後に「tokenId」に「id」、「value」にコンテンツの「price」をnumberに変換して設定ます

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FZ_I_7EWdi.png?alt=media)

これでマーケットプレイスからの「購入」の実装ができました！



### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `#section-1` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 3 点を記載してください ✨

    1. 質問が関連しているセクション番号とレッスン番号
    2. 何をしようとしていたか
    3. エラー文をコピー&ペースト
    4. エラー画面のスクリーンショット
    

* * *

環境設定が完了したら、次のレッスンに進んでください 🎉