```markdown
# ADBatteryStatus 🚀

**ADBatteryStatus** is a unique battery alarm application designed for Android
that runs seamlessly on Linux. Unlike typical battery alarm apps that operate 
solely on Android devices, ADBatteryStatus offers a smooth experience on Linux 
systems, making it a versatile tool for users.

## Features 🌟

- 📊 Monitor the battery percentage of Android devices.
- 🔔 Alarm notifications when the battery needs charging.
- ⚡ Alarm notifications when the battery can be unplugged.
- 💬 Message box alerts on Linux computers.
- 🎶 Audio alarms on both Linux computers and Android devices for a dual alert system.
- 🔄 Automatic switching between USB and TCP ADB server modes without manual configuration.
- 🔌 Identify the power source of the charger (USB or AC adapter).
- 👤 No root user privileges required; regular users can run the application.
- 🌐 No internet connection needed for operation.
- 🔒 Safe for the user's Linux system.
- 🌡️ Monitor Android battery temperature and notify users (available from version 1 onwards).
- 💬 Customizable quotes displayed on the Linux screen.
- 🎥 Full-screen video mode in Firefox will still display quotes and alarms.
- ⏰ Automatic crontab creation if ADBatteryStatus is not configured.
- 🔧 Enable or disable quotes and notifications through a configuration file.
- 📈 Different icons for charging and non-charging states based on battery percentage.
- 🔊 Adjustable speaker volume settings in the configuration file.
- 🤖 ADBatteryStatus can verbally announce the battery percentage to users.
- 🔕 Option to disable alarm notifications during specific hours.

## Installation 🛠️

1. **Download the ADBatteryStatus file** and extract it to the `~/Music/alarm` directory.
2. **Set permissions** to execute the file:
   ```bash
   chmod +x adbatterystatus
   ```
3. **Configure crontab** to run ADBatteryStatus:
   ```bash
   crontab -e
   ```
   Add the following line to run ADBatteryStatus every 5 minutes:
   ```bash
   */5 * * * * ~/Music/alarm/adbatterystatus 30 98 your_ip:5555 43
   ```

Crontab will run batmeter99 every 5 minutes. The purpose of this crontab 
scriptis so that the batmeter can provide an alarm when the android battery 
needs to be charged or needs to be removed from the charger when it has reached 
the maximum level of charging the android battery.

## Usage 📖

Run ADBatteryStatus using the terminal:
```bash
./adbatterystatus min_charge_level max_unplug_level ip_wifi_android:port_adb warm_temp
```

### Example Command:
```bash
./adbatterystatus 30 98 192.168.43.1:5555 43
```

## Setup and Configuration ⚙️

The `adbatterystatus` file needs to be configured to run in the Linux terminal 
using the following command:

```bash
chmod +x adbatterystatus

This command grants execute permissions to the file. To enable audio alarms on 
the Android device, two audio files—needcharged.ogg and releasecable.ogg—must be 
placed in the sdcard/Download directory, such as sdcard/Download/pasangcas.ogg 
and sdcard/Download/lepascas.ogg. If these files are not set up on the Android 
device, it is not a problem; however, adbatterystatus will not execute audio 
alerts on the Android device.

ADBatteryStatus can detect the source of the charger, whether it is from a 
computer's USB port or an AC adapter connected to the power outlet. The 
application will automatically identify the Android device or tablet using the 
connected charger. To ensure everything runs smoothly, users need to enable the 
developer options on their Android device. When the USB device is connected to 
the computer, the program will utilize this connection to monitor the battery 
status. Additionally, if a TCP connection is used, it can also provide alerts 
when the Android device's battery needs charging.

## Requirements 📋

- `amixer`
- Desktop Environment: `xfce`
- `mpg123`
- `ogg123`

## Contributing 🤝

We welcome contributions! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file 
for details.

## Contact 📬

For any inquiries, please reach out to [duitmoro@yahoo.com](mailto:duitmoro@yahoo.com).

---

Thank you for checking out ADBatteryStatus! We hope it enhances your Android 
experience on Linux! 🎉
```
