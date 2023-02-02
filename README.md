# Surface Laptop 3 Intel Opencore

Support OS:
- Mac OS Ventura 13.x
- Mac OS Montery 12.x

Adapted from [Repo](https://github.com/badstorm/surface-pro-7-opencore) with the following changes:
- Changed the USB Mapping to correct Surface Laptop 3 USB layout. The origianl mapping cannot achieve 10GB speed for USBC.
- Remove CPU type so that it can support any CPU.



### Surface Spec
- Intel Core i7-1065G7 processor
- 16 GB Memory
- Intel® Iris™ Plus
- SSD 512 GB


### Status
|  Status             |         Feature                 |            Note                      |
|---------------------|---------------------------------|--------------------------------------|
|  :white_check_mark: |  Graphic Acceleration          |  QE/CI works |
|  :white_check_mark: |  Wifi & Bluetooth              |  With [OpenIntelWireless](https://github.com/OpenIntelWireless/itlwm) |
|  :white_check_mark: |  Type Cover  (keyboard/mouse)  |  With RHUB and [BigSurface](https://github.com/Xiashangning/BigSurface)|
|  :white_check_mark: |  Audio                         |  With AppleALC   |
|  :white_check_mark: |  Battery Status          |  With [BigSurface](https://github.com/Xiashangning/BigSurface)                 |
|  :white_check_mark: |  Touch & Stylus          |  With [BigSurface](https://github.com/Xiashangning/BigSurface). You need to manualy insall [IPTSDaemon](https://github.com/Xiashangning/IPTSDaemon)                |
|                     |                                |                   |
|  :white_check_mark: |  Camera Front        |                   |


### Known Issues
- Unable to enter S3 sleep. All Surface products only support S0 sleep, and the current EFI does not enable S0 sleep.
- Background noise after waking from sleep when running on battery. Playing any sound can stop the noise.
- Unable to pair with some bluetooth devices, such as MX Master 3. (Ventura only, see this: [Issue](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/issues/421#issuecomment-1413191342))
- Surface Dock does not work at all.


### Install Notes
- For a better Wifi experience, use **itlwm** instead of **AirportItlwm** with [HeliPort](https://github.com/OpenIntelWireless/HeliPort) (Simple enable/disable them in `config.plist`)
- For better trackpad support go to `System Preferences -> Trackpad` and disable `Force click and haptic feedback`


### Secure Boot
If you want to boot without the anoing red bar with the lock icon you can try [this workaround](https://github.com/badstorm/surface-pro-7-opencore/blob/master/SecureBoot.With.Grub.md). *Thanks to @Xiashangning*
