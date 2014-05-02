---
layout: post
title:  "YouTube動画の再生時間を取得するサンプル"
date:   2014-05-02 00:10:00
categories: website
tags: JavaScript YouTube
---

YouTube JavaScript Player APIを使って、ホームページにYouTubeの動画を埋め込む & 再生時間を取得するサンプルをつくりました。→ [http://jsdo.it/saxsir/30zA][2]

[![サンプルページ](//farm8.staticflickr.com/7295/14082687851_477d048279.jpg)][2]

---

# Tips（追記@2014年5月2日01:30）
jsdo.itじゃないけど、別のサーバーで同じことをやろうとしたら動画再生時に

```console
Ad adLoadError error: No ads were found in the ad response. At least one ad is required to be able to load or play. errorCode: 1001
```

と怒られた。2014年5月2日時点で結構同じことで困ってる人もいるようで解決策がなかなか見つからなかったが、偶然

```js
var youtubeUrl = 'http://www.youtube.com/v/h03Sxiv6zzk?enablejsapi=1'
```

を

```js
var youtubeUrl = 'https://youtube.googleapis.com/v/h03Sxiv6zzk?enablejsapi=1'
```
にしたら直った。
たぶん原因は、読み込み先のURLがhttpだったから？（確証なし）


[1]: http://bit.ly/1n6VZ7U
[2]: http://bit.ly/1mhnPNb
