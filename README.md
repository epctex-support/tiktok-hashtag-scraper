[https://apify.com/epctex/tiktok-hashtag-scraper](https://apify.com/epctex/tiktok-hashtag-scraper?fpr=yhdrb)

# Actor - Tiktok Hashtag Scraper

## Tiktok Hashtag scraper

Since Tiktok doesn't provide a good and free API, this actor should help you to retrieve data from it.

The Tiktok Hashtag data scraper supports the following features:

-   Search any hashtag - Any hashtags can be scraped by keywords.

-   Scrape video - Scrape any video from Tiktok and retrieve all the data from it.

-   Music Details - Get any music information that is used in the video.

-   User details - Retrieve all user-related information.

## Bugs, fixes, updates, and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/tiktok-hashtag-scraper/issues).

## Input Parameters

The input of this scraper should be JSON containing the list of pages on the Tiktok Hashtag that should be visited. Possible fields are:

- `search`: (Optional) (String) List of TikTok Hashtag keywords. You can type any hashtag here to search. URLs.

- `startUrls`: (Optional) (Array) List of TikTok Hashtag URLs. You should only provide the URLs of hashtags. URLs.

- `endPage`: (Optional) (Number) Final number of page that you want to scrape. The default is `Infinite`. This applies to all `search` requests and `startUrls` individually.

- `maxItems`: (Optional) (Number) You can limit scraped items. This should be useful when you search through the big lists or search results.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

- `extendOutputFunction`: (Optional) (String) Function that takes a JQuery handle ($) as an argument and returns an object with data.

- `customMapFunction`: (Optional) (String) Function that takes each object's handle as an argument and returns the object with executing the function.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Compute Unit Consumption

The actor is optimized to run blazing fast and scrape many listings as possible. Therefore, it forefronts all listing detail requests. If the actor doesn't block very often it'll scrape 100 listings in 2 minutes with ~0.03-0.07 compute units.

### Tiktok Hashtag Scraper Input example

```json
{
  "search":[
    "anime",
    "tiktok"
  ],
  "startUrls":[
    "https://www.tiktok.com/search?q=%23music&t=1670685477846",
    "https://www.tiktok.com/search?q=%23dance&t=1670685484412",
    "https://www.tiktok.com/search?q=%23challenge&t=1670685494590"
  ],
  "maxItems": 20,
  "endPage":2,
  "proxy":{
    "useApifyProxy":true
  }
}

```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with a failure state and output an explanation of what is wrong.

## Tiktok Hashtag Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any language (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Tiktok Hashtag actor.

## Other Tiktok Scrapers

If you need different functionalities or all at once, we have solutions for each of them. You can check;

- [Tiktok Hashtag Scraper](https://apify.com/epctex/tiktok-video-scraper?fpr=yhdrb)
- [Tiktok Search Scraper](https://apify.com/epctex/tiktok-search-scraper?fpr=yhdrb)
- [Tiktok Hashtag Scraper](https://apify.com/epctex/tiktok-hashtag-scraper?fpr=yhdrb)

## Scraped Tiktok Hashtag Properties

The structure of each item in the Tiktok Hashtag looks like this:

### Item Detail

```json
{
    "url": "https://www.tiktok.com/@argenby/video/7171782248281165058?is_copy_url=1&is_from_webapp=v1",
    "id": "7171782248281165058",
    "desc": "Sigma must respect everyone… @ayazkyzz @aman4ek ",
    "createTime": "1669810686",
    "scheduleTime": 0,
    "video": {
        "id": "7171782248281165058",
        "height": 1024,
        "width": 576,
        "duration": 25,
        "ratio": "720p",
        "cover": "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/68bcbf3c77cf4c1abceb5451670efe9b_1669810691?x-expires=1670684400&x-signature=19jHqqG6eFPiKGsWpTl09QMs5FI%3D",
        "originCover": "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/5265105283774571951c21641d63f7cb_1669810691?x-expires=1670684400&x-signature=lQJXmi8BL1DlujrxK3zDZ9zpNgI%3D",
        "dynamicCover": "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/562a22832c644852ba8d347a9fa68bed_1669810689?x-expires=1670684400&x-signature=htSWcF3Wfmn7JtwSujVlnfWiA%2B0%3D",
        "playAddr": "https://v16-webapp-prime.us.tiktok.com/video/tos/alisg/tos-alisg-pve-0037c001/o8H4gXOGWCfQpA4jmDeovDBgMDICAe2sCPlPHu/?a=1988&ch=0&cr=0&dr=0&lr=tiktok_m&cd=0%7C0%7C1%7C0&cv=1&br=4120&bt=2060&cs=0&ds=3&ft=ebLH6H-qMyq8ZChdvhe2NQn7fl7Gb&mime_type=video_mp4&qs=0&rc=O2VkZjc8OzU5Ojo7Zmk1OkBpamk0Zzc6ZnRuaDMzODczNEAyLTIwNS4tXl8xMmAuYGEzYSNvY2NscjRvZzBgLS1kMS1zcw%3D%3D&expire=1670685681&l=202212100920562B270FF34D9A7E100CE7&policy=2&signature=ae4d9e7729c1d307c91933b888c6e3e8&tk=tt_chain_token",
        "downloadAddr": "https://v16-webapp-prime.us.tiktok.com/video/tos/alisg/tos-alisg-pve-0037c001/o8H4gXOGWCfQpA4jmDeovDBgMDICAe2sCPlPHu/?a=1988&ch=0&cr=0&dr=0&lr=tiktok_m&cd=0%7C0%7C1%7C0&cv=1&br=4120&bt=2060&cs=0&ds=3&ft=ebLH6H-qMyq8ZChdvhe2NQn7fl7Gb&mime_type=video_mp4&qs=0&rc=O2VkZjc8OzU5Ojo7Zmk1OkBpamk0Zzc6ZnRuaDMzODczNEAyLTIwNS4tXl8xMmAuYGEzYSNvY2NscjRvZzBgLS1kMS1zcw%3D%3D&expire=1670685681&l=202212100920562B270FF34D9A7E100CE7&policy=2&signature=ae4d9e7729c1d307c91933b888c6e3e8&tk=tt_chain_token",
        "shareCover": [
            "",
            "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/5265105283774571951c21641d63f7cb_1669810691~tplv-tiktok-play.jpeg?x-expires=1671267600&x-signature=Z7zBNqfs9L2Vo6srGOwbkIEuBpQ%3D",
            "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/5265105283774571951c21641d63f7cb_1669810691~tplv-tiktokx-share-play.jpeg?x-expires=1671267600&x-signature=PGYZjPcWk%2BcjUVJZ%2FpnBrDUfkNU%3D"
        ],
        "reflowCover": "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/68bcbf3c77cf4c1abceb5451670efe9b_1669810691?x-expires=1670684400&x-signature=19jHqqG6eFPiKGsWpTl09QMs5FI%3D",
        "bitrate": 2110249,
        "encodedType": "normal",
        "format": "mp4",
        "videoQuality": "normal",
        "encodeUserTag": "",
        "codecType": "h264",
        "definition": "720p",
        "subtitleInfos": [],
        "zoomCover": {
            "240": "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/68bcbf3c77cf4c1abceb5451670efe9b_1669810691~tplv-efzqqlc8t1-1:240:240.jpeg?x-expires=1670684400&x-signature=t0DwDvAPehjM7Ob53BYd12gBwJQ%3D",
            "480": "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/68bcbf3c77cf4c1abceb5451670efe9b_1669810691~tplv-efzqqlc8t1-1:480:480.jpeg?x-expires=1670684400&x-signature=li0pGwN7DJsD4%2FmJdc4a3yRnMO4%3D",
            "720": "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/68bcbf3c77cf4c1abceb5451670efe9b_1669810691~tplv-efzqqlc8t1-1:720:720.jpeg?x-expires=1670684400&x-signature=FDV%2FAbhnT%2FGbQmL4Ivb3x4mP8Jg%3D",
            "960": "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/68bcbf3c77cf4c1abceb5451670efe9b_1669810691~tplv-efzqqlc8t1-1:960:960.jpeg?x-expires=1670684400&x-signature=ywEhRnhhMWtLpwR3KNSIonCDbho%3D"
        },
        "volumeInfo": {
            "Loudness": -10.1,
            "Peak": 1
        },
        "bitrateInfo": [
            {
                "GearName": "normal_720_0",
                "Bitrate": 2110249,
                "QualityType": 10,
                "PlayAddr": {
                    "Uri": "v10044g50000ce3kjqrc77u4odf1ffrg",
                    "UrlList": [
                        "https://v16-webapp-prime.us.tiktok.com/video/tos/alisg/tos-alisg-pve-0037c001/o8H4gXOGWCfQpA4jmDeovDBgMDICAe2sCPlPHu/?a=1988&ch=0&cr=0&dr=0&lr=tiktok_m&cd=0%7C0%7C1%7C0&cv=1&br=4120&bt=2060&cs=0&ds=3&ft=ebLH6H-qMyq8ZChdvhe2NQn7fl7Gb&mime_type=video_mp4&qs=0&rc=O2VkZjc8OzU5Ojo7Zmk1OkBpamk0Zzc6ZnRuaDMzODczNEAyLTIwNS4tXl8xMmAuYGEzYSNvY2NscjRvZzBgLS1kMS1zcw%3D%3D&expire=1670685681&l=202212100920562B270FF34D9A7E100CE7&policy=2&signature=ae4d9e7729c1d307c91933b888c6e3e8&tk=tt_chain_token",
                        "https://v19-webapp-prime.us.tiktok.com/video/tos/alisg/tos-alisg-pve-0037c001/o8H4gXOGWCfQpA4jmDeovDBgMDICAe2sCPlPHu/?a=1988&ch=0&cr=0&dr=0&lr=tiktok_m&cd=0%7C0%7C1%7C0&cv=1&br=4120&bt=2060&cs=0&ds=3&ft=ebLH6H-qMyq8ZChdvhe2NQn7fl7Gb&mime_type=video_mp4&qs=0&rc=O2VkZjc8OzU5Ojo7Zmk1OkBpamk0Zzc6ZnRuaDMzODczNEAyLTIwNS4tXl8xMmAuYGEzYSNvY2NscjRvZzBgLS1kMS1zcw%3D%3D&expire=1670685681&l=202212100920562B270FF34D9A7E100CE7&policy=2&signature=ae4d9e7729c1d307c91933b888c6e3e8&tk=tt_chain_token"
                    ],
                    "DataSize": "6755701",
                    "UrlKey": "v10044g50000ce3kjqrc77u4odf1ffrg_h264_720p_2110249",
                    "FileHash": "d92737d2ac38c33ddebd9e0afbaa6593",
                    "FileCs": "c:0-22092-a553"
                },
                "CodecType": "h264"
            }
        ]
    },
    "author": "argenby",
    "music": {
        "id": "7171782257949100801",
        "title": "оригинальный звук",
        "playUrl": "https://sf16-ies-music-sg.tiktokcdn.com/obj/tiktok-obj/7171782259232492289.mp3",
        "coverLarge": "https://p16-sign-sg.tiktokcdn.com/aweme/1080x1080/tos-alisg-avt-0068/4a8c54d6baa5732d083aaca3ef871734.jpeg?x-expires=1670835600&x-signature=1yrZ6Qf7Hy%2FsRU6rULfsXXp2p2s%3D",
        "coverMedium": "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/4a8c54d6baa5732d083aaca3ef871734.jpeg?x-expires=1670835600&x-signature=Aa3Tky6X%2B3m%2FangEhsOCzFPJDrA%3D",
        "coverThumb": "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/4a8c54d6baa5732d083aaca3ef871734.jpeg?x-expires=1670835600&x-signature=m9DMmC2OoErr30FkK76n1j7TIEw%3D",
        "authorName": "argenby • sigma",
        "original": true,
        "duration": 25,
        "album": "",
        "scheduleSearchTime": 0
    },
    "challenges": [],
    "stats": {
        "diggCount": 7400000,
        "shareCount": 13600,
        "commentCount": 62600,
        "playCount": 70000000
    },
    "isActivityItem": false,
    "duetInfo": {
        "duetFromId": "0"
    },
    "warnInfo": [],
    "originalItem": false,
    "officalItem": false,
    "textExtra": [
        {
            "awemeId": "",
            "start": 29,
            "end": 38,
            "hashtagId": "",
            "hashtagName": "",
            "type": 0,
            "subType": 0,
            "userId": "6526453173618480128",
            "isCommerce": false,
            "userUniqueId": "ayazkyzz",
            "secUid": "MS4wLjABAAAAfxkLilz8ohRQ1sdJmUBGm-CTC92gUnqUmBPQbX0mw5tRBQ66s0ybk7XDJTu-q14g"
        },
        {
            "awemeId": "",
            "start": 39,
            "end": 47,
            "hashtagId": "",
            "hashtagName": "",
            "type": 0,
            "subType": 0,
            "userId": "6788380939058152454",
            "isCommerce": false,
            "userUniqueId": "aman4ek",
            "secUid": "MS4wLjABAAAAvM3JCM3glBxhKEgmyFDAjTwgFp5mGBsKUM9Vjq8WGJ3zqwMNg94yG8bXT5MZKkOr"
        }
    ],
    "secret": false,
    "forFriend": false,
    "digged": false,
    "itemCommentStatus": 0,
    "showNotPass": false,
    "vl1": false,
    "takeDown": 0,
    "itemMute": false,
    "effectStickers": [],
    "authorStats": {
        "followerCount": 8900000,
        "followingCount": 138,
        "heart": 268000000,
        "heartCount": 268000000,
        "videoCount": 1248,
        "diggCount": 75700
    },
    "privateItem": false,
    "duetEnabled": true,
    "stitchEnabled": true,
    "stickersOnItem": [],
    "isAd": false,
    "shareEnabled": true,
    "comments": [],
    "duetDisplay": 0,
    "stitchDisplay": 0,
    "indexEnabled": true,
    "diversificationLabels": [
        "Scripted Drama",
        "Scripted Drama",
        "Performance"
    ],
    "adAuthorization": false,
    "adLabelVersion": 0,
    "locationCreated": "KG",
    "nickname": "argenby • sigma",
    "authorId": "6891947725971571713",
    "authorSecId": "MS4wLjABAAAAXNAIWPpSImEnNOEvlPDEdFw34qRbdmXBr5k80rQmgScYjyKYi911PDUuNb5l5p_4",
    "avatarThumb": "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/4a8c54d6baa5732d083aaca3ef871734.jpeg?x-expires=1670835600&x-signature=m9DMmC2OoErr30FkK76n1j7TIEw%3D",
    "downloadSetting": 0,
    "authorPrivate": false
}
```

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that are available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
