### 👩‍💻 **Mint,List,Buyを各画面で実装**

ここでは、各画面ごとでMint,List,BuyのFunctionを呼び出す実装を行なっていきます。

**実装する画面**

*   マイNFTコンテンツページ
こちらのページでは、MintされたもののMarketplaceへは「List」されていないアイテムをマーケットプレイスに「List」していきます。
BunzzSDKを通じて、「approve」と「list」関数を呼び出して行きます。


### **マイNFTコンテンツページ**

「NFTコンテンツ作成ページ」で作成されたNFTはまだマーケットプレイスに公開されていないため、NFTマーケットプレイスに公開していきますが、マーケットプレイスへの公開にあたり「承認」と「公開」の2つの手順が必要となるのですが、1つのBunzzSDKでは、1つの関数までしか呼び出すことができないため、本ページでは2つのBunzzSDKを配置しています。


**Workflow画面へ移動します**

まずは、Bubbleない画面のWorkflow画面へ遷移しましょう。
画面左側に縦に並んでいるタブの上から2つ目にある「Workflow」を選択してください。


#### **マーケットプレイスへの承認**

まず、「Publish」ボタンがクリックされたときにマーケットプレイスへの「承認」を行いますが、　「Lesson1」同様Bunzzの「Update action」を設定します

Workflow画面には、「When」と書かれている正方形のボックスが並んでいますので、「Button Publish is clicked」と書かれているボックスをクリックしてください。
クリックすると、正方形のボックス下部に「Step1」などの長方形のボックスが出てくるので、「Step1」の「Update Action BunzzSDK A」を選択してください。
すると黒色のpropertyが立ち上がります。
確認して次のステップへ進んでください。

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FlrCdwhM62.png?alt=media)


次に「Module Name」　と「Function Name」を設定してapprove関数を呼び出す準備をしていきます。
- 「Module Name」に「NFT(ERC721)」を入力します（今回は入力されています）
- 「Function Name」に「approve」を入力します（今回は入力されています）

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FBaNtKPy1h.png?alt=media)


ここで一度Bunzzの「Dashboard」に戻り、マーケットプレイスの「address」を取得します
「Dashboard」は画面左側の「Function」配下にあります。

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FY2oZDcU8W.png?alt=media)

Bubbleの画面に戻り、「argument」に「to」と「tokenId」を設定していきます。

「argument」に「to」と「tokenId」を設定していきます。
- 「to」に先ほどBunzzの「Dashboard」で取得したマーケットプレイスの「address」を入力します
- 「tokenId」にコンテンツの「id」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FcPy2euIkt.png?alt=media)

これでマーケットプレイスへの「承認」の実装ができましたので、次に「公開」するための実装を行っていきます

#### **マーケットプレイスへの公開**

マーケットプレイスへの公開は、先ほど実装した「承認」（approve）が完了した後に処理が走る必要があるため、完了したことをトリガーにしたイベントである「BunzzSDK A Complete Update Action」が設定されています。
また、この時の注意点として冒頭で記載した通り1つのBunzzSDKでは、1つの関数しか呼び出すことができないため、「BunzzSDK A Complete Update Action」が呼び出されたときのactionには、「approve」の際に呼び出されたBunzzSDKとは別のBunzzSDKを呼び出す必要があります。

2つ目のBunzzSDKとして、「BunzzSDK B」を呼び出す「Update Action」を設定していきます。

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2F2wh9wlBe0.png?alt=media)


次に「Module Name」　と「Function Name」を設定してlist関数を呼び出す準備をしていきます。
- 「Module Name」に「Simple Marketplace (For NFT)」を入力します（今回は入力されています）
- 「Function Name」に「list」を入力します（今回は入力されています）


![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FbrewDNnWM.png?alt=media)


最後に「argument」に「tokenId」と「price」を設定していきます。
- 「tokenId」にコンテンツの「id」を設定します
- 「price」にコンテンツの「price」をnumber型に変換して設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FvLnT54Pm8.png?alt=media)

これでマーケットプレイスにアイテムが公開されました！



### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `#section-2` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 3 点を記載してください ✨

    1. 質問が関連しているセクション番号とレッスン番号
    2. 何をしようとしていたか
    3. エラー文をコピー&ペースト
    4. エラー画面のスクリーンショット
    

* * *

環境設定が完了したら、次のレッスンに進んでください 🎉
