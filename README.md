<p align="center">
  <img src="https://github.com/Apparence-io/ricoh_theta/raw/main/.github/img/logo.jpg" alt="ricoh_theta logo" />
</p>
<br><br>

<p align="center">
  <a href="https://pub.dev/packages/ricoh_theta"><img src="https://img.shields.io/pub/v/ricoh_theta" alt="pub dev ricoh_theta"></a>
</p>
<br>
<hr>
<br>

## 🚀&nbsp; Overview

Use your **Ricoh Theta** device in your Flutter app very easily.

- 📱 Support both **iOS** and **Android**
- 🎥 Direct **live preview**
- 🎚 Adjust **FPS** for preview in realtime
- 📸 Take a **picture** & show thumbnail
- 🔋 Get device **battery level** 
- ℹ️ Fetch **device information**
- 📁 Retrieve device **files** from storage
- 🌆 **View** photo in high resolution

## 📖&nbsp; Installation

### Install the package
```sh
flutter pub add ricoh_theta
```

### Import the package
```dart
import 'package:ricoh_theta/ricoh_theta.dart';
```

## 🚀&nbsp; Get started

- Create an instance of the plugin
```dart
final _ricohThetaPlugin = RicohTheta();
```

- Init the connection to the camera by setting IP address of the device
```dart
await _ricohThetaPlugin.setTargetIp("192.168.1.1");
```

> Don't forget to connect your phone device to the [WiFi camera](https://support.theta360.com/es/catalog/easy_instructions.pdf) before any calls to the plugin.

## 🗃&nbsp; Available calls


| Param                | Type                                   | Description                                                                                 | Required |
|----------------------|----------------------------------------|---------------------------------------------------------------------------------------------|----------|
| setTargetIp          | ```Future```                           | set IP address to the camera & init connection (required before any calls)                  | ✅       |
| disconnect           | ```Future```                           | disconnect from the device                                                                  |          |
| startLiveView        | ```Future```                           | start capture of live view                                                                  |          |
| removeImageWithFileId | ```Future<bool?>```                   | remove an image from storage device                                                         |          |
| getImage             | ```Future<File?>```                    | get an image in high resolution from storage device                                         |          |
| pauseLiveView        | ```Future```                           | pause capture of live view                                                                  |          |
| stopLiveView         | ```Future```                           | stop capture of live view                                                                   |          |
| resumeLiveView       | ```Future```                           | resume capture of live view                                                                 |          |
| batteryLevel         | ```Future<num>```                      | get battery level in percent from device                                                    |          |
| getDeviceInfo        | ```Future<DeviceInfo?>```              | return the current device information like model, firmware & serial number                  |          |
| getStorageInfo       | ```Future<StorageInfo?>```             | return information about the device storage                                                 |          |
| update               | ```Future```                           | update device session, can be used to keep a session alive                                  |          |
| getImageInfoes       | ```Future<List<ImageInfoes>>```        | return information about images stored on the device                                        |          |
| takePicture          | ```Future<String?>```                  | take a picture & return a thumbnail path                                                    |          |
| listenCameraImages   | ```Stream<Uint8List>?```               | listen for live preview images coming from the device                                       |          |
| listenDownloadProgress  | ```Stream<num>?```                  | listen for download progress of images                                                      |          |
| adjustLiveViewFps    | ```Future```                           | adjust fraps per seconds for image preview                                                  |          |

> ```adjustLiveViewFps``` method is used to not surcharge the device, you can set 0 to skip this feature.

## 📣&nbsp; Sponsor
<img src="https://github.com/Apparence-io/bart/raw/master/.github/img/apparence_logo.png" alt="logo apparence io" />
<br />
<br />

[Initiated and sponsored by Apparence.io.](https://apparence.io)

## 👥&nbsp; Contribution

Contributions are welcome.
Contribute by creating a PR or create an issue 🎉.