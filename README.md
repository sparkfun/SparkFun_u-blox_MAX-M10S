SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic)
===========================================================

[![SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic)](https://cdn.sparkfun.com/assets/parts/1/7/3/4/1/18037-SparkFun_GNSS_Receiver_Breakout_-_MAX-M10S__Qwiic_-01_Default.jpg)](https://www.sparkfun.com/products/18037)

[*SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic) (GPS-18037)*](https://www.sparkfun.com/products/18037)

The SparkFun MAX-M10S Breakout is an ultra-low-power, high performance, miniaturized GNSS board that is perfect for battery operated applications that don't possess a lot of space, such as asset trackers and wearable devices. The MAX-M10S module from u-blox has an extremely low power consumption that is less than 25mW in continuous tracking mode.

The on-board MAX-M10S GNSS receiver can receive signals from the GPS, GLONASS, BeiDou, and Galileo constellations. Thanks to the u-blox Super-S technology, the module offers improved RF sensitivity with small antennas and in non-line-of-sight scenarios. We've included an SMA connector for a sturdy connection when attaching an external antenna. The board is also equipped with an on-board rechargeable battery that provides backup power to the module's RTC. This reduces the time-to-first fix from a cold start (~24s) to a hot start (~1s). The battery will maintain RTC and GNSS orbit data without being connected to power for up to five hours. This increases precision and decreases lock time in battery operated devices without compromising GNSS performance.

Additionally, this u-blox receiver supports I2C which makes it perfect for Qwiic compatibility so we don't have to use up our precious UART ports. Utilizing our handy Qwiic system, no soldering is required to connect it to the rest of your system. However, we still broke out 0.1"-spaced pins in case you prefer to use a breadboard. For users that prefer to communicate over UART, we made sure to configure the UART pin grouping to an industry standard to ensure that it easily connects to a Serial Basic.

U-blox based GNSS products are configurable using the popular Windows program called u-center. Plenty of different functions can be configured on the MAX-M10S: baud rates, update rates, spoofing detection, external interrupts, etc. We've also written an extensive Arduino library for u-blox modules to make reading and controlling the MAX-M10S over our Qwiic Connect System easy. Leave NMEA behind! Start using a much lighter weight binary interface and give your microcontroller (and its one serial port) a break. The SparkFun Arduino library shows how to read latitude, longitude, even heading and speed over I2C without the need for constant serial polling.

Repository Contents
-------------------

* **/Documents** - Related U-blox datasheets and various whitepapers 
* **/Hardware** - Eagle files

Documentation
--------------

* **[Installing an Arduino Library Guide](https://learn.sparkfun.com/tutorials/installing-an-arduino-library)** - Basic information on how to install an Arduino library.
* **[Arduino Library](https://github.com/sparkfun/SparkFun_u-blox_GNSS_Arduino_Library)** - Arduino Library for u-blox modules.
* **[Hookup Guide](https://learn.sparkfun.com/tutorials/1759)** - Hookup guide for the SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic).

Product Versions
----------------
* [GPS-18037](https://www.sparkfun.com/products/18037)

Version History
---------------
* v1.0 - Initial Release

License Information
-------------------

This product is _**open source**_! 

Various bits of the code have different licenses applied. Anything SparkFun wrote is beerware; if you see me (or any other SparkFun employee) at the local, and you've found our code helpful, please buy us a round!

Please use, reuse, and modify these files as you see fit. Please maintain attribution to SparkFun Electronics and release anything derivative under the same license.

Distributed as-is; no warranty is given.

- Your friends at SparkFun.
