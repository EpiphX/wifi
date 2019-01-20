# wifi

This plugin allows Flutter apps to get wifi ssid and list, connect wifi with ssid and password.

This plugin works Android.

iOS later released.



Sample usage to check current status:

```dart
import 'package:wifi/wifi.dart';

String ssid = await Wifi.ssid;

//Signal strength， 1-3，The bigger the number, the stronger the signal
int level = await Wifi.level;

String ip = await Wifi.ip;

var result = await Wifi.connection('ssid', 'password');

// Only works on Android.
// 'key' is used to filter the list. Use empty string if the full wifi list is desired.
List<WifiResult> list = await Wifi.list('key');
```
When you use connection on iOS (iOS 11 only)

1. 'build Phase' -> 'Link Binary With Libraries' add 'NetworkExtension.framework'
    ![NetworkExtension](https://github.com/once10301/wifi/blob/master/png/NetworkExtension.png)

2. in 'Capabilities' open 'Hotspot Configuration'

    ![NetworkExtension](https://github.com/once10301/wifi/blob/master/png/Hotspot%20Configuration.png)

3. If you device is iOS12, in 'Capabilities' open 'Access WiFi Information'

    ![NetworkExtension](https://github.com/once10301/wifi/blob/master/png/Access%20WiFi%20Information.png)

If you want to use Wifi.list on iOS, 

reference http://baixin.io/2017/01/iOS_Wifilist/

## Getting Started

For help getting started with Flutter, view our online
[documentation](https://flutter.io/).

For help on editing plugin code, view the [documentation](https://flutter.io/developing-packages/#edit-plugin-package).
