We've broken out the u-blox MAX-M10S module to a breakout. This section highlights the relevant features of the board. For more information about the IC, check out the Resources and Going Further.


<div class="center-block text-center"><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic_u-blox_Module.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic_u-blox_Module.jpg" alt="MAX-M10S Highlighted"></a></div>


### Power

Power for this board should be **3.3V**. There is a 3.3V pin on the PTH header along the side of the board, but you can also provide power through the Qwiic connector.

<table class="table table-hover table-striped table-bordered">
  <tr align="center">
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_Power.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_Power.jpg" alt="Top View of Power Highlighted"></a></td>
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_Power.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_Power.jpg" alt="Bottom View of Power Highlighted"></a></td>
  </tr>
  <tr align="center">
  <td><i>Top View</i></td>
  <td><i>Bottom View</i></td>
  </tr>
</table>





### Communication Ports

<div class="alert alert-warning" role="alert">
  <b>Note: </b>The MAX-M10S differs from other modules as it only has I<sup>2</sup>C and UART. It is important to note that the board does not have SPI pins.
</div>

<div class="center-block text-center"><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic.jpg" alt="Back of Board I2C and UART Ports, but no SPI"></a></a></div>

### Qwiic and I<sup>2</sup>C (a.k.a. DDC)

There are two PTHs labeled `SDA` and `SCL` which indicates the I<sup>2</sup>C data lines. Similarly, you can just use the Qwiic connector to provide power and connect to the I<sup>2</sup>C pins. The [Qwiic ecosystem](https://www.sparkfun.com/qwiic) is made for fast prototyping by removing the need for soldering. All you need to do is plug a Qwiic cable into the Qwiic connector and voila!

<table class="table table-hover table-striped table-bordered">
  <tr align="center">
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_I2C.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_I2C.jpg" alt="Top View of I2C"></a></td>
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_I2C.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_I2C.jpg" alt="Bottom View of I2C"></a></td>
  </tr>
  <tr align="center">
  <td><i>Top View</i></td>
  <td><i>Bottom View</i></td>
  </tr>
</table>

<div class="alert alert-info" role="alert">
  <b>Note:</b> The only I2C address for this and all u-Blox GPS products is <b>0x42</b>, though each can have their address changed through software.
</div>




### UART

For users that prefer to communicate over UART, we made sure to configure the UART pin grouping to an industry standard to ensure that it easily connects to a [Serial Basic](https://www.sparkfun.com/products/15096). Extra UART pins are also broken out on another edge of the board as well. The port is set to **38400 baud** as the default.

<table class="table table-hover table-striped table-bordered">
  <tr align="center">
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_UART.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_UART.jpg" alt="Top View of UART"></a></td>
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_UART.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_UART.jpg" alt="Bottom View of UART"></a></td>
  </tr>
  <tr align="center">
  <td><i>Top View</i></td>
  <td><i>Bottom View</i></td>
  </tr>
</table>



### Control Pins

These pins are used for various extra control of the MAX-M10S. The control pins are highlighted below.

<table class="table table-hover table-striped table-bordered">
  <tr align="center">
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_Control_Pins.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_Control_Pins.jpg" alt="Top View of Control Pins"></a></td>
   <td><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_Control_Pins.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_Control_Pins.jpg" alt="Bottom View of Control Pins"></a></td>
  </tr>
  <tr align="center">
  <td><i>Top View</i></td>
  <td><i>Bottom View</i></td>
  </tr>
</table>

* **PPS:** Pulse-per-second output pin. Begins blinking at 1Hz when module gets basic GPS/GNSS position lock.
* <b><span style="text-decoration: overline">RST</span>:</b> Reset input pin. Pull this line low to reset the module.
* <b><span style="text-decoration: overline">SAFE</span>:</b> Safeboot input pin. This is required for firmware updates to the module and generally should not be used or connected. To save on space, the silkscreen is labeled on the bottom of the board.
* **EINT:** Interrupt input/output pin. Can be configured using U-Center to bring the module out of deep sleep or to output an interrupt for various module states.





### SMA Connector for Antenna

The board is populated with an SMA connector for a secure connection to a patch antenna.

<div class="center-block text-center"><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_SMA_Connector.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_SMA_Connector.jpg" alt="SMA Antenna"></a></div>


### LEDs

The board includes two status LEDs as indicated in the image below.

<div class="center-block text-center"><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_LEDs.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_LEDs.jpg" alt="LEDs"></a></div>

* **PPS:** The pulse per second LED will illuminate each second once a position lock has been achieved.
* **PWR:** The power LED will illuminate when 3.3V is provided either over the Qwiic bus or any of the 3.3V PTH pins.





### Jumpers

There are four jumpers on the back of the board. For more information, check out our [tutorial on working with jumper pads and PCB traces](https://learn.sparkfun.com/tutorials/how-to-work-with-jumper-pads-and-pcb-traces/all) should you decide to cut the traces with a hobby knife.

<div class="center-block text-center"><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_Jumpers.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Bottom_Jumpers.jpg" alt="Jumpers"></a></div>


* **PWR:** This is connected to the PWR LED on the top of the board. Cutting this disables the LED.
* **MEAS:** Short for current measurement. By default, the MEAs is closed. Cutting the jumper and soldering to the PTH pads will allows you to insert a current meter and precisely monitor the how much current your application is consuming.
* **PPS:** This is connected to the PPS LED on the top of the board. Cutting this disables the LED.
* **I<sup>2</sup>C:** The I<sup>2</sup>C jumpers are open by default. By adding solder to the jumpers, it will connect to the 2.2k&ohm; pull-up resistors for the I<sup>2</sup>C bus.  Most of the time you can leave these alone unless your project requires you to [connect the pull-up resistors](https://learn.sparkfun.com/tutorials/i2c/all#i2c-at-the-hardware-level).





### Backup Battery

The MS621FE rechargeable battery maintains the battery backed RAM (BBR) on the GNSS module. This allows for much faster position locks (a.k.a. hot start). The BBR is also used for module configuration retention. The battery is automatically trickle charged when power is applied and should maintain settings and GNSS orbit data for up to two weeks without power.

<div class="center-block text-center"><a href="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_Backup_Battery.jpg"><img src="..assets/18037-SparkFun_GNSS_Receiver_Breakout_MAX-M10S_Qwiic-Top_Backup_Battery.jpg" alt="Backup Battery"></a></div>





### Board Dimensions

The overall length and width with the antenna connector is about 1.74" x 1.20". There are four mounting holes by each corner of the board.

<div class="center-block text-center"><a href="https://cdn.sparkfun.com/assets/e/8/8/9/8/SparkFun_u-blox_MAX-M10S_Board_Dimensions.png"><img src="https://cdn.sparkfun.com/r/600-600/assets/e/8/8/9/8/SparkFun_u-blox_MAX-M10S_Board_Dimensions.png" alt="Board Dimensions"></a></div>
