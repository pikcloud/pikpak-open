# PikPak Android SDK for Telegram Development Guide

Please first know what is [PikPak Android SDK for Telegram](sdk-for-telegram-android.md).  
You can use the SDK for development by following the steps below.

## Step1. Get SDK
1. Read and confirm that you agree to [PikPak Open SDK Developer Service Agreement](sdk-developer-service-agreement.md). 
1. Send an email to dev@mypikpak.com in the following format to apply for the SDK:
    
    - Email title: `Apply for PikPak Android SDK for Telegram`
    - Email body:
    > I have read and agreed to the PikPak Open SDK Developer Service Agreement and apply to obtain PikPak Android SDK for Telegram. My App information is as follows:  
    App introduction: ________  
    App download page address: ________  
    App owner contact email: ________  
    App package name: ________  
    App signature md5 hash: ________  
    I promise that the above information is true and correct, please review my application.
    
    Please fill in each underlined space in the body of the email with correct and true information. Sending an email means that you fully agree with the content of the email.

    It should be noted that we may simply ignore applications with obvious missing or incorrect information. Even if complete information is provided, we may reject it because the App is not suitable or does not currently require more SDK integration, or we may ask for more supplementary information.

1. If the application is approved, you will get the download link of the SDK dedicated to your App in the email reply. The SDK is provided as an [Android Archive (AAR)](https://developer.android.com/studio/projects/android-library#aar-contents) file, download it.

## Step2. Add SDK to Your Project
1. Integrate the downloaded SDK AAR file into your Telegram android Project. You can refer to [1](https://developer.android.com/studio/projects/android-library#psd-add-aar-jar-dependency) or [2](https://stackoverflow.com/questions/16682847/how-to-manually-include-external-aar-package-using-gradle-for-android). The Telegram android App package name and signature md5 hash must be consistent with those provided during application.
1. Add other dependencies to your Telegram android project. You can refer to [this](https://developer.android.com/build/dependencies#dependency-types). If these dependencies already exist in the project, there is no need to add them again.
    ```
    implementation('org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.8.10')
    implementation('android.arch.lifecycle:extensions:' + '1.1.1')
    implementation('com.google.android.material:material:1.4.0')
    implementation('androidx.appcompat:appcompat:1.4.2')
    implementation('androidx.legacy:legacy-support-v4:1.0.0')
    implementation('androidx.constraintlayout:constraintlayout:2.1.4')
    implementation('androidx.core:core-ktx:1.8.0')
    implementation('androidx.viewpager2:viewpager2:1.1.0-beta01')
    implementation('androidx.annotation:annotation:1.2.0')
    implementation('androidx.biometric:biometric:1.1.0')
    implementation('androidx.lifecycle:lifecycle-runtime-ktx:2.2.0-alpha02')
    implementation('androidx.core:core-splashscreen:1.0.0')
    implementation('androidx.startup:startup-runtime:1.1.1')
    implementation('com.google.android.gms:play-services-auth:20.2.0')
    implementation('com.google.android.gms:play-services-auth-api-phone:18.0.1')
    implementation('com.google.android.gms:play-services-identity:18.0.1')
    implementation('com.google.android.gms:play-services-base:18.1.0')
    implementation('com.google.code.gson:gson:2.8.5')
    implementation platform('com.google.firebase:firebase-bom:32.1.0')
    implementation('com.google.firebase:firebase-dynamic-links')
    implementation('com.google.firebase:firebase-analytics')
    implementation('com.google.firebase:firebase-auth')
    implementation('com.google.firebase:firebase-messaging')
    implementation('com.google.android.play:core:1.10.0')
    implementation('com.google.firebase:firebase-crashlytics')
    implementation('com.google.firebase:firebase-crashlytics-ndk')
    implementation('com.google.firebase:firebase-perf')
    implementation('com.google.android.gms:play-services-ads-identifier:17.0.1')
    implementation('com.github.tiann:FreeReflection:3.1.0')
    implementation('com.github.bumptech.glide:glide:4.15.1')
    implementation('com.github.bumptech.glide:okhttp3-integration:4.15.1')
    implementation('jp.wasabeef:glide-transformations:4.3.0')
    implementation('com.tencent.mars:mars-xlog:1.2.6')
    implementation('com.squareup.okhttp3:okhttp:' + '3.12.13')
    implementation('com.facebook.android:facebook-login:12.0.1')
    implementation('com.facebook.android:facebook-android-sdk:12.0.1')
    implementation('com.android.billingclient:billing:5.1.0')
    implementation('com.xiaomi.billingclient:billing:1.1.0')
    implementation('com.airbnb.android:lottie:6.0.0')
    implementation('io.github.scwang90:refresh-layout-kernel:2.0.5')
    implementation('io.github.scwang90:refresh-header-classics:2.0.5')
    implementation('com.meituan.android.walle:library:' + '1.1.7')
    implementation('com.meituan.android.walle:payload_reader:1.1.7')
    implementation('com.alibaba:arouter-api:1.5.2')
    implementation('com.github.hufeiyang.Android-AppLifecycleMgr:applifecycle-api:1.0.4')
    implementation('io.github.jeremyliao:live-event-bus-x:1.8.0')
    implementation('com.yanzhenjie:sofia:1.0.5')
    implementation('com.tencent.bugly:crashreport:4.1.9.2')
    implementation('com.tencent.bugly:nativecrashreport:3.9.2')
    implementation('com.googlecode.libphonenumber:libphonenumber:8.12.57')
    implementation('com.klinkerapps:link_builder:2.0.5')
    implementation('com.github.jenly1314:zxing-lite:2.4.0')
    implementation('com.tencent:mmkv:1.2.16')
    implementation('com.adjust.sdk:adjust-android:4.33.4')
    implementation('com.paypal.checkout:android-sdk:0.112.0')
    implementation('com.getkeepsafe.relinker:relinker:1.4.5')
    implementation('io.github.idisfkj:android-startup:1.1.0')
    implementation('com.github.Jay-Goo:RangeSeekBar:v3.0.0')
    implementation('io.github.knight-zxw:spwaitkiller:0.0.8')
    implementation('org.lsposed.hiddenapibypass:hiddenapibypass:4.3')
    implementation('org.greenrobot:greendao:3.3.0')
    implementation('org.fourthline.cling:cling-core:2.1.1')
    implementation('org.fourthline.cling:cling-support:2.1.1')
    implementation('org.eclipse.jetty:jetty-server:8.1.22.v20160922')
    implementation('org.eclipse.jetty:jetty-client:8.1.22.v20160922')
    implementation('org.eclipse.jetty:jetty-servlet:8.1.22.v20160922')
    implementation('org.bouncycastle:bcprov-jdk15on:1.60')
    implementation('com.tencent.mm.opensdk:wechat-sdk-android-without-mta:6.7.0')
    implementation('com.android.installreferrer:installreferrer:2.2')
    implementation('com.aliyun.dpa:oss-android-sdk:2.9.13')
    implementation('cloud.xbase.sdk:core:2.0.1.200201')
    ```

## Step3. Use the SDK in Your Project
1. Add the sdk interface calling code in your Telegram android project as needed. 
    - Import SDK classes in your code
    ```
    import com.pikcloud.tgapplib.PPSDKFacade;
    ```

    - Implement the required interfaces defined by the SDK, and Call methods of SDK classes, for example
    ```
    PPSDKFacade.addMessageToDrive(context, ...);
    ```

    The required interfaces and available methods are listed in the [following paragraphs](#sdk-interface-reference).

1. Build and Debug your Telegram android project. 

## SDK Interface Reference

### Available Methods
- void PPSDKFacade.attachBaseContext(android.app.Application application, TGHostInterface tgHostInterface);

    Register the TGHostInterface class that needs to be implemented.

- void PPSDKFacade.onCreate(android.app.Application application);

    Notify the application created.

- void PPSDKFacade.onTerminate(android.app.Application application);

    Notify the application terminated.

- void PPSDKFacade.onTrimMemory(android.app.Application application, int level);

    Notify the application trimed memory.

- void PPSDKFacade.onLowMemory(android.app.Application application);

    Notify the application low-memory happened.

- void PPSDKFacade.onConfigurationChanged(android.app.Application application, @NonNull android.content.res.Configuration newConfig);

    Notify the application configuration changed.

- void PPSDKFacade.onTGLogout(String tgUserId);

    Notify the current Telegram account logout.
    - tgUserId: Telegram account user id

- void PPSDKFacade.onTGAccountSwitch(String oldTgUserId, String newTgUserId);
    
    Notify the current Telegram account changed.
    - oldTgUserId: Telegram account user id before changing
    - newTgUserId: Telegram account user id after changing

- void PPSDKFacade.addMessageToDrive(android.content.Context context, TGMessageFile tgMessageFile);

    Store a file from a message to PikPak cloud drive.
    - context: Current calling context
    - tgMessageFile: The file information

- void PPSDKFacade.play(android.content.Context context, TGMessageFile tgMessageFile);

    Play a certain file via PikPak.
    - context: Current calling context
    - tgMessageFile: The file information

- void PPSDKFacade.downloadToLocal(android.content.Context context, TGMessageFile tgMessageFile);

    Download a file to the device via PikPak.
    - context: Current calling context
    - tgMessageFile: The file information

- void PPSDKFacade.getVipStatus(android.content.Context context, String tgUserId, PPVipStatusCallback callback);
    
    Query whether the PikPak account bound to the current Telegram account is a PikPak premium account.
    - tgUserIdList: Telegram account user id
    - callback: Query result callback

- void PPSDKFacade.getFriendVipStatus(android.content.Context context, List<String> tgUserIdList, PPVipStatusListCallback callback);
    
    Batch query whether the PikPak accounts bound to the accounts of friends of the current Telegram account are premium accounts.
    - context: Current calling context
    - tgUserIdList: Telegram account user id list
    - callback: Query result callback

- void PPSDKFacade.navigateToPage(android.content.Context context, String path, Bundle param);
    
    Opens the specified PikPak function or user interface.
    - context: Current calling context
    - path: Path to PikPak function or user interface
        - Main page -> path: "/drive/main_tab", param: {"tab":0}
        - Transfer -> path: "/drive/main_tab", param: {"tab":1}
        - File list -> path: "/drive/main_tab", param: {"tab":2}
        - My page -> path: "/drive/main_tab", param: {"tab":3}
        - Create cloud download -> path: "/drive/task/create", param: {"url": "Cloud download link filled in the input box, can be empty"}
        - Downloads on device -> path: "/download/task_list", param: null
        - Purchase Premium -> path: "/account/pay_activity", param: {"refer_from": "", "aid_from": ""}
    - param: Parameters corresponding to the path

- TGHostInterface getTGHostInterface();

    Get registered TGHostInterface class.

### Required Interface to be Implemented
```
public interface TGHostInterface {
    /**
     * PikPak account Premium status has changed
     * @param isVip: Whether the new status is Premium
     */
    void onPPVipChange(boolean isVip);

    /**
     * The binding status of PikPak account and Telegram account has changed
     * @param isBind: Whether it has been bound
     */
    void onPPBindStatusChange(boolean isBind);

    /**
     * Start the specified bot
     * @param botId: Specified bot id
     * @param botUrl: Specified bot link URL
     */
    void startBot(String botId, String botUrl);

    /**
     * Send a text message to the specified Bot
     * @param botId: Specified bot id
     * @param text: Text message to sent
     */
    void sendTextToBot(String botId, String botUrl, String text);

    /**
     * Forward a file in a message to the specified Bot
     * @param botId: Specified bot id
     * @param groupId: The group id or channel id of the messageid
     * @param messageId: message id
     * @param fileId: file id
     */
    void sendFileToBot(String botId, String botUrl, String groupId, String messageId, String fileId);

    /**
     * Forward the entire message to the specified bot
     * @param botId: Specified bot id
     * @param groupId: The group id or channel id of the messageid
     * @param messageId: message id
     */
    void sendMessageToBot(String botId, String botUrl, String groupId, String messageId);

    /**
     * Get the text of the latest messages of the specified bot
     * @param botId: Specified bot id
     * @param count: Messages count
     * @return List of messages containing text content
     */
    List<String> getBotLatestMessage(String botId, String botUrl, int count);
}
```

### Predefined Classes (Documentation WIP)
```
public static class TGMessageFile {
    public String groupId;
    public String messageId;
    public String fileId;
    public String mimeType;
    public String text;
    public String fileName;
    public long fileSize;
    public String fileThumbnail;
    public String from;
    public String fileExtensionName;
    public String toString();
}

public static class VipStatusBean {
    public String tgUserId;
    public boolean isVip;
    public String expire;
}

public interface PPVipStatusListCallback {
    void onVipStatusCallback(int ret, String errorContent, String errorKey, List<VipStatusBean> statusList);
}

public interface PPVipStatusCallback {
    void onVipStatusCallback(int ret, String errorContent, String errorKey, VipStatusBean status);
}
```