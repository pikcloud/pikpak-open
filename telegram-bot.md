# Post Content on Telegram by PikPak Bot

## Introductions

In Telegram, we provide the "[Save To PikPak](https://t.me/pikpak_bot)" Bot (`PikPak-Bot`) to support user simply forwarding and saving. Furthermore, we also use [Telegram Bot Deeplink](https://core.telegram.org/bots/#deep-linking) to provide any content publisher with the function of calling `PikPak-Bot` more quickly, even if the user haven't added `PikPak-Bot` yet. Users can jump to the Bot by the link, click start button of the bot, then Picking and Packing the content step by step.

Currently this function only supports [bit torrent](https://en.wikipedia.org/wiki/BitTorrent) content posted in the form of [magnet link](https://en.wikipedia.org/wiki/Magnet_URI_scheme). The steps for publishing content are as follows:

1. Prepare and publish the content in the form of Bit Torrent, get the magnet link and ensure that it can be downloaded.

2. Get the `BitTorrent info-hash` string in the magnet link (at the "xt" parameter value, excluding "urn:btih:" prefix), splice it into `PikPak-Bot` Deeplink according to the following format:

    ```text
    https://t.me/pikpak_bot?start=magnet_[INFO-HASH-STRING]
    ```

    [INFO-HASH-STRING] is the BitTorrent info-hash string.

    for example, for the following magnet link:

    ```text
    magnet:?xt=urn:btih:c12fe1c06bba254a9dc9f519b335aa7c1367a88a
    ```

    The following PikPak-Bot Deeplink can be made:

    ```text
    https://t.me/pikpak_bot?start=magnet_c12fe1c06bba254a9dc9f519b335aa7c1367a88a
    ```

    > *Tip: Why not use the complete magnet link directly in `PikPak-Bot` Deeplink?*  
    > *Because the start parameter of Telegram Bot Deeplink has a length limitation (64 characters), and cannot contain special characters such as ":", "?", refer to [this](https://core.telegram.org/bots/#deep-linking).*

3. Include the `PikPak-Bot` Deeplink obtained above in Telegram messages, which can be private chat, public group or channel etc. People who receives the message could clicking on the link to jump to `PikPak-Bot` and start Picking and Packing the content you posted.

## Precautions

Welcome to publish content through the above PikPak Open method, but the content publisher must understand and accept the [PikPak User Agreement](https://mypikpak.com/policy/user-agreement), especially please pay attention to the legality requirements of the posted content and the relevant provisions of intellectual property protection.
