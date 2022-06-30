### 👩‍💻 **Mint,List,Buyを各画面で実装**

ここでは、各画面ごとでMint,List,BuyのFunctionを呼び出す実装を行なっていきます。

**実装する画面**

*   マイNFTコンテンツページ



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



### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `#section-1` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 3 点を記載してください ✨

    1. 質問が関連しているセクション番号とレッスン番号
    2. 何をしようとしていたか
    3. エラー文をコピー&ペースト
    4. エラー画面のスクリーンショット
    

* * *

環境設定が完了したら、次のレッスンに進んでください 🎉
