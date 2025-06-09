## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能  
機能：日本の郵便番号から住所を検索できる無料APIです  
エンドポイント:https://zipcloud.ibsnet.co.jp/api/searchに対して、郵便番号をしてすることにより  
対応する住所情報（都道府県、市区町村、町域）が取得できます。  
* リクエストとレスポンスのフォーマット  
リクエストフォーマット:https://zipcloud.ibsnet.co.jp/api/search?zipcode=1000001  
レスポンスフォーマット:{
  "message": null,
  "results": [
    {
      "zipcode": "1000001",
      "prefcode": "13",
      "address1": "東京都",
      "address2": "千代田区",
      "address3": "千代田",
      "kana1": "ﾄｳｷｮｳﾄ",
      "kana2": "ﾁﾖﾀﾞｸ",
      "kana3": "ﾁﾖﾀﾞ"
    }
  ],
  "status": 200
}  
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL  
名称：ラーメンAPI  
参照URL：https://ramen-api.dev  
* エンドポイントと機能  
エンドポイント：https://ramen-api.dev/shops/  
機能:登録されているラーメン屋をローマ字で入力すると、店名とラーメンの写真を表示する。  
* リクエストとレスポンスのフォーマット  
リクエストフォーマット例:https://ramen-api.dev/shops/yoshimuraya  
レスポンスフォーマット例:
{
  "shop": {
    "id": "yoshimuraya",
    "name": "吉村家",
    "photos": [
      {
        "name": "yoshimuraya-001.jpg",
        "url": "https://ramen-api.dev/images/yoshimuraya/yoshimuraya-001.jpg",
        "width": 1200,
        "height": 900,
        "authorId": "yusukebe"
      }
    ]
  }
}

### Q3-3. 感想
* 今回の課題で苦労したこと  
apiの呼び出しを行う際のスクリプトの組み方、及び呼び出したAPIからの返答をどのようにして画面表示させるかに苦労し、特に5-2課題に関しては、写真を表示させるスクリプトをどのように組めば良いかを思い付くのに多くの時間を要した。
* 演習を通して理解できたこと  
APIの呼び出し方、呼び出したAPIからの返答を画面出力させる方法、フォーマットの仕組みについて理解した。
* Web APIの利便性や課題など  
利便性:Web APIを使うことで、外部の最新データを簡単にWebページに組み込める  
課題:APIの仕様が変更されたり、停止された場合の対応が必要。  
