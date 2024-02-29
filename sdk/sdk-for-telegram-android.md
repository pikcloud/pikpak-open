# PikPak Android SDK for Telegram

## Introductions
We aspire to seamlessly integrate into the vibrant ecosystem of content transmission, storage, and consumption tools. Our goal is to share our capabilities with anyone or any platform in need.

Telegram, an excellent and popular globally-oriented instant messaging application. Furthermore, Telegram itself embraces openness. Not only is its offical app open source, but it also supports apps developed by third-party as unofficial Telegram clients. Currently, several unofficial Telegram apps are thriving.

Telegram has been a part of PikPak’s journey from the very beginning. We provide the "[Save To PikPak](https://t.me/pikpak_bot)" Telegram Bot (`PikPak-Bot`) to support user simply forwarding files and saving it, or [post content](telegram-bot.md). For the moment `PikPak-Bot` has become a distinctive feature, and we’re delighted that users appreciate it.

However, Telegram Bot’s interactive capabilities have limitations. The process of transferring files from Telegram to PikPak and consuming them can be cumbersome, requiring frequent switching between apps. To enhance the user experience of using PikPak as a personal cloud drive within the Telegram app, we’ve experimentally developed the `PikPak Android SDK for Telegrams`. By integrating this SDK, unofficial Telegram Android apps can seamlessly enjoy almost all of PikPak’s features within their own interface.

With the SDK in place, transferring Telegram files to the PikPak cloud drive remains facilitated by the `PikPak-Bot`. However, the SDK streamlines the entire process, allowing direct access to PikPak’s original app features without leaving the current app.

## Features
1. Quickly send files from your chat to the PikPak cloud drive.
1. Automatically start playback or initiate downloads after saving files.
1. One-click registration and binding of your PikPak account, or authorization to link an existing PikPak account via the PikPak app.
1. Display the complete main interface of the embedded PikPak App.
1. Call various functions of the embedded PikPak.

## Usage
Please refer to [Development Guide](sdk-for-telegram-android-development-guide.md).

## Precautions
- By downloading or using our SDK, you agree to [PikPak Open SDK Developer Service Agreement](sdk-developer-service-agreement.md). Please refrain from using the SDK for malicious or illegal purposes. Do not integrate it into apps that violate [PikPak User Agreement](https://mypikpak.com/policy/user-agreement) and [PikPak Privacy Policy](https://mypikpak.com/en-US/policy/privacy-policy).
- This is an ongoing experimental project, and both interfaces and features may evolve in the future. We cannot guarantee its stability.
- This SDK is prepared for experienced Android App developers. If you encounter any issues during integration, feel free to submit an issue in this repository. However, real-time technical support is not yet available.
