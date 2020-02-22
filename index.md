## Welcome to Ayra's Sticker Maker

Here is guide to make Sticker for WhatsApp.

Before we get started, make sure you're install [Ayra's Sticker Maker](https://github.com/AyraHikari/ayra_sticker_maker/releases/)

# Auto Maker (Telegram/Line Stickers)

1. Copy Telegram/Line sticker
2. Go to [@AyraStickersBot](https://t.me/AyraStickersBot)
3. Paste that link in that bot

# Manual Maker (Advanced)

To make this stickers, you need to have learn:
1. Resize images
2. Convert images to webp
3. Known what json is and known how to __parse__ that
4. Zip package

## Download Stickers

### Download Telegram Stickers

- You can use any bots from Telegram to download that, or
- [Use this tool](https://github.com/Cartmanishere/telegram-sticker-downloader) to download Stickers

### Download Line Stickers

- See [this guide](https://github.com/doubleplusc/Line-sticker-downloader) to download Line Stickers

### Create Your Own Stickers

- You need to be a good designer to do this
- Make sure image is 96 x 96 pixels
- Max file size of 50KB
- Export file to webp (Recommended)

## Create A WhatsApp Package

1. Create a folder as you like
2. Copy max 30 sticker images to that folder, if you have above 30 stickers, create a new folder again, then copy again
```
Examples:
 ├ stickers_1 (30 stickers)
 ├ stickers_2 (30 stickers)
 └ stickers_3 (5 stickers)
```
3. Create a images that for tray (any stickers, example stickers_1_1.webp as tray, so rename tray.webp)
4. Make sure all folders have all trays
```
Examples:
 ├ stickers_1 (have tray.webp)
 ├ stickers_2 (have tray.webp)
 └ stickers_3 (have tray.webp)
```

## Create A JSON

1. Create a new file, and write like this
```
{
    "android_play_store_link": "https://play.google.com/store/apps/details?id=me.ayra.stickermaker",
    "ios_app_store_link": "",
    "sticker_packs": []
}
```
- *android_play_store_link*: Link that for playstore (DO NOT CHANGE THIS, else your sticker will be invaild)
- *ios_app_store_link*: Like above, since we use for Android, leave it blank
- *sticker_packs*: To fill in bellow guide

2. Create a new file again, and write like this
```
{
  "identifier": "stickers_1",
  "name": "Animals",
  "publisher": "Ayra's Sticker Maker",
  "tray_image_file": "tray.webp",
  "publisher_email": "",
  "publisher_website": "https://github.com/AyraHikari/ayra_sticker_maker/",
  "privacy_policy_website": "",
  "license_agreement_website": "",
  "stickers": []
}
```
- *identifier*: Folder stickers, like guide above, fill *stickers_1*
- *name*: Your sticker pack name
- *publisher*: Your damn name
- *tray_image_file*: Fill tray.webp if you named that tray as tray
- *publisher_email*: Your damn email, can be blank
- *publisher_website*: Your website, leave it there or fill blank as you like
- *privacy_policy_website*: Fill if you have
- *license_agreement_website*: Read above
- *stickers*: To fill in bellow guide

3. Create a new file again, to make your damn sticker work, do this
```
{
  "image_file": "sticker_1.webp",
  "emojis": ["\ud83d\ude03"]
}
```
- *image_file*: Your sticker file name
- *emojis*: Emoji should be escaped unicode, see [Gemoji](https://github.com/wooorm/gemoji/blob/master/support.md) and copy paste that `Escaped unicode` to this

4. After follow guide above, fill all code to one
```
Example:
{
    "android_play_store_link": "https://play.google.com/store/apps/details?id=com.ayra.stickermaker",
    "ios_app_store_link": "",
    "sticker_packs": [{
        "identifier": "stickers_1",
        "name": "Animals",
        "publisher": "Ayra's Sticker Maker",
        "tray_image_file": "tray.webp",
        "publisher_email": "AyraHikari@linuxmail.org",
        "publisher_website": "https://github.com/AyraHikari/ayra_sticker_maker/",
        "privacy_policy_website": "",
        "license_agreement_website": "",
        "stickers": [{
            "image_file": "sticker_1.webp",
            "emojis": ["\ud83d\ude03"]
        }, {
            "image_file": "sticker_2.webp",
            "emojis": ["\ud83d\ude03"]
        }]
    }, {
        "identifier": "stickers_2",
        "name": "Animals 2",
        "publisher": "Ayra's Sticker Maker",
        "tray_image_file": "tray.webp",
        "publisher_email": "AyraHikari@linuxmail.org",
        "publisher_website": "https://github.com/AyraHikari/ayra_sticker_maker/",
        "privacy_policy_website": "",
        "license_agreement_website": "",
        "stickers": [{
            "image_file": "sticker_3.webp",
            "emojis": ["\ud83d\ude03"]
        }, {
            "image_file": "sticker_4.webp",
            "emojis": ["\ud83d\ude03"]
        }]
    }]
}
```

5. Save as `contents.json`, then you have package like bellow
```
Examples:
 ├ stickers_1
 ├ stickers_2
 ├ stickers_3
 └ contents.json
```

## Make A Package

1. Zip that package, then rename `.zip` to `.ayrawapack`
```
Examples:
 ├ stickers_1
 ├ stickers_2
 ├ stickers_3
 ├ contents.json
 └ my_stickers.ayrawapack
```
2. Transfer to your phone, open file manager, open `my_stickers.ayrawapack`, then open as *Ayra's Sticker Maker* to import that sticker

# Import WhatsApp Stickers

Just open a file name `.ayrawapack`, then select *Ayra's Sticker Maker* app, it will import your stickers
