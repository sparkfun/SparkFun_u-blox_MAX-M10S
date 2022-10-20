
<div class="alert alert-info">
<b>Note:</b> This example assumes you are using the latest version of the Arduino IDE on your desktop. If this is your first time using Arduino, please review our tutorial on <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">installing the Arduino IDE.</a> If you have not previously installed an Arduino library, please check out our <a href="https://learn.sparkfun.com/tutorials/installing-an-arduino-library">installation guide.</a><br /><br />


If you've never connected an FTDI or CH340 to your computer before, you may need to install drivers for the USB-to-serial converter. Check out our <a href="https://learn.sparkfun.com/tutorials/how-to-install-ftdi-drivers">How to Install FTDI Drivers</a> or <a href="https://learn.sparkfun.com/tutorials/sparkfun-serial-basic-ch340c-hookup-guide#drivers-if-you-need-them">How to Install CH340 Drivers</a> tutorial for help with the installation.
</div>

All of our u-blox based GPS boards share the same library: this board, their [predeccesors](https://learn.sparkfun.com/tutorials/sparkfun-gps-breakout-zoe-m8q-and-sam-m8q-hookup-guide) and the higher [precision](https://www.sparkfun.com/products/15005) [u-blox cousins](https://www.sparkfun.com/products/15136). The SparkFun u-blox Arduino library can be downloaded with the Arduino library manager by searching '**SparkFun u-blox GNSS**' or you can grab the zip here from the [GitHub repository](https://github.com/sparkfun/SparkFun_u-blox_GNSS_Arduino_Library) to manually install:

<div class="text-center"><a class="btn btn-danger" href="https://github.com/sparkfun/SparkFun_u-blox_GNSS_Arduino_Library/archive/main.zip" role="button" target="u-blox_library">SparkFun U-blox Arduino Library (ZIP)</a></div>
<br />

There are several example sketches provided that utilize the I<sup>2</sup>C bus to get you up and receiving messages from space. We&apos;ll go over one of the examples in this tutorial.

<div class="alert alert-info" role="alert">
  <strong>Note: </strong> Example 2 uses the '<b>MicroNMEA</b>' library by <b>Steve Marple</b>. Make sure to install the library as well by searching for it in the Arduino library manager. You could also grab the zip here from the <a href="https://github.com/stevemarple/MicroNMEA">GitHub repository</a> to manually install.
<br /><br />

<div class="text-center"><a class="btn btn-primary" href="https://github.com/stevemarple/MicroNMEA/archive/master.zip" role="button" target="micronmea">MicroNMEA Arduino Library (ZIP)</a></div>
</div>
