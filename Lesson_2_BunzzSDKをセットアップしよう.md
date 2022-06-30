### 👩‍💻 **DappのID/API Keyをアプリ側に設定**

ここでは、BunzzSDKのプラグインをBubbleにインストールして、アプリケーションサイドに設定していきます。

**今回行うこと**

1.  Bubbleの各画面にBunzzSDKを設定


### **Bunzz SDKを各画面に設定**

#### **Bunzzを設定するページ**

*   NFTコンテンツ作成ページ
*   マイNFTコンテンツページ
*   NFTコンテンツページ

#### **各ページで設定する必要があるSetup方法からご紹介します**

Bubbleにて設定する前に「Dapp ID」と「API Key」を取得するためBunzzに戻り、画面左側の「Client SDK」をクリックします

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2F9a2eu8p0h.png?alt=media)

再び、Bubbleに移り、各ページ毎に「Bunzz SDK」を設定していきます。

まず、画面左側のVisual elements より「Bunzz SDK」を画面に設置し、先ほど取得した「Dapp ID」と「API Key」をそれぞれ入力します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FcsZWQn3uI.png?alt=media)

次にWorkflow画面に移り、Setupを行いますが、ページが読み込まれた際にSetupが行われるように「Page is loaded」のactionに「Setup BunzzSDK」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2FU-ut81exL.png?alt=media)

Setupが完了したら、addressを取得するのですが、Bunzzの方で「Bunzz SDK Setup Completed」というSetupが完了した際に設定できるEventを用意してくれているので、これを使い、actionに「Get Signer Address」を設定します

![](https://firebasestorage.googleapis.com/v0/b/hideaki-97c59.appspot.com/o/images%2FhX626yFRzBaLxKfnu0ejxujjhv93%2Ffmf5ZGIxk.png?alt=media)

これで各画面におけるセットアップが完了です！


### 🙋‍♂️ 質問する

ここまでの作業で何かわからないことがある場合は、Discord の `#section-1` で質問をしてください。

ヘルプをするときのフローが円滑になるので、エラーレポートには下記の 3 点を記載してください ✨

    1. 質問が関連しているセクション番号とレッスン番号
    2. 何をしようとしていたか
    3. エラー文をコピー&ペースト
    4. エラー画面のスクリーンショット
    

* * *

環境設定が完了したら、次のレッスンに進んでください 🎉
