The [SparkFun u-blox MAX-M10S breakout](https://www.sparkfun.com/products/18037) is an ultra-low-power, high performance, miniaturized GNSS board that is perfect for battery operated applications that don't possess a lot of space, such as asset trackers and wearable devices. In this tutorial, we will quickly get you set up using the Qwiic ecosystem and Arduino so that you can start reading the output!

<div style="text-align: center">
  <table style="border-style:none">
    <tr>
      <td>
        <a href="https://www.sparkfun.com/products/18037">
          <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/7/3/4/1/18037-SparkFun_GNSS_Receiver_Breakout_-_MAX-M10S__Qwiic_-01_Default.jpg" alt="SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic)" height="500px"></div>
          <div style="text-align: left"><h3 class="title">SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic)</h3></div>
        </a>
        <div style="text-align: left"><span>GPS-18037</span></div>
      </td>
    </tr>
  </table>
  </div>

<div style="text-align: center"><iframe width="600" height="328" src="https://www.youtube.com/embed/Yh8pLKs7aaY" title="Product Showcase: SparkFun GNSS Receiver MAX-M10S" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>





### Required Materials

To follow along with this tutorial, you will need the following materials. You may not need everything though depending on what you have. Add it to your cart, read through the guide, and adjust the cart as necessary.

<div>
<table style="border-style:none">
    <tr>
        <td width="140">
            <a href="https://www.sparkfun.com/products/18037">
              <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/7/3/4/1/18037-SparkFun_GNSS_Receiver_Breakout_-_MAX-M10S__Qwiic_-01_Default.jpg" alt="SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic)" height="140"></div>
              <h3 style="text-align: left">SparkFun GNSS Receiver Breakout - MAX-M10S (Qwiic)</h3>
            </a>
            <span>GPS-18037</span>
        </td>
        <td width="140">
            <a href="https://www.sparkfun.com/products/14986">
              <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/3/2/9/0/14986-GPS_GNSS_Magnetic_Mount_Antenna_SMA_-_3m-01.jpg" alt="GPS/GNSS Magnetic Mount Antenna - 3m (SMA)" height="140"></div>
              <h3 style="text-align: left">GPS/GNSS Magnetic Mount Antenna - 3m (SMA)</h3>
            </a>
            <span>GPS-14986</span>
        </td>
        <td width="140">
            <a href="https://www.sparkfun.com/products/18158">
              <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/7/4/8/7/18158-SparkFun_RedBoard_Plus-01.jpg" alt="SparkFun RedBoard Plus" height="140"></div>
              <h3 style="text-align: left">SparkFun RedBoard Plus</h3>
            </a>
            <span>DEV-18158</span>
        </td>
        <td width="140">
            <a href="https://www.sparkfun.com/products/14426">
              <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/2/4/5/2/14426-Qwiic_Cable_-_50mm-01.jpg" alt="Qwiic Cable - 50mm" height="140"></div>
              <h3 style="text-align: left">Qwiic Cable - 50mm</h3>
            </a>
            <span>PRT-14426</span>
        </td>
    </tr>
    <tr>
    <td width="140">
        <a href="https://www.sparkfun.com/products/15424">
          <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/3/9/8/3/15424-Reversible_USB_A_to_C_Cable_-_2m-01.jpg" alt="Reversible USB A to C Cable - 2m" height="140"></div>
          <h3 style="text-align: left">Reversible USB A to C Cable - 2m</h3>
        </a>
        <span>CAB-15424</span>
    </td>
    </tr>
</table>
</div>



#### Additional GPS Antenna Options

Below are some other GPS antenna options.

<div class="container">
<table style="border-style:none;">
    <tr >
    <td width="140">
        <a href="https://www.sparkfun.com/products/14987">
          <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/3/2/9/1/14987-GPS_GNSS_Embedded_Antenna_SMA_-_1m-01a.jpg" alt="GPS/GNSS Embedded Antenna - 1m (SMA)" height="140"></div>
          <h3 style="text-align: left">GPS/GNSS Embedded Antenna - 1m (SMA)</h3>
        </a>
        <span>GPS-14987</span>
    </td>
    <td width="140">
        <a href="https://www.sparkfun.com/products/177">
          <div style="text-align: center"><img src="https://cdn.sparkfun.com//assets/parts/1/4/7/00177-02.jpg" alt="GPS Embedded Antenna SMA" height="140"></div>
            <h3 style="text-align: left">GPS Embedded Antenna SMA</h3>
        </a>
        <span>GPS-00177</span>
    </td>
    </tr>
</table>
</div>



### Suggested Reading

If you aren't familiar with the Qwiic system, we recommend reading [here for an overview](https://www.sparkfun.com/qwiic).

<div style="text-align: center">
<table class="table table-bordered">
  <tr align="center">
   <td style="vertical-align: middle"><a href="https://www.sparkfun.com/qwiic"><img src="https://cdn.sparkfun.com/r/457-457/assets/learn_tutorials/8/2/Qwiic-registered-black.png" alt="Qwiic Connect System" title="Click to learn more about the Qwiic Connect System!"></a></td>
  </tr>
  <tr align="center">
    <td><i><a href="https://www.sparkfun.com/qwiic">Qwiic Connect System</a></i></td>
  </tr>
</table>
</div>

If you aren’t familiar with the following concepts, we also recommend checking out a few of these tutorials before continuing.

<table style="border-style:none">
    <tr>
        <td align="center" width="264">
            <a href="https://learn.sparkfun.com/tutorials/gps-basics">
            <img src="https://cdn.sparkfun.com/c/264-148/assets/3/6/6/f/7/50edfc17ce395f7105000000.jpg"><h3 class="title">GPS Basics</h3></a>
        </td>
        <td align="center" width="264">
            <a href="https://learn.sparkfun.com/tutorials/i2c">
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/8/2/I2C-Block-Diagram.jpg"><h3 class="title">I2C</h3></a>
        </td>
        <td align="center" width="264">
            <a href="https://learn.sparkfun.com/tutorials/serial-basic-hookup-guide">
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/5/9/7/14050-01.jpg"><h3 class="title">Serial Basic Hookup Guide</h3></a>
        </td>
        <td align="center" width="264">
            <a href="https://learn.sparkfun.com/tutorials/redboard-plus-hookup-guide">
            <img src="https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/7/5/8/18158-SparkFun_RedBoard_Plus-01.jpg"><h3 class="title">RedBoard Hookup Guide</h3></a>
        </td>
    <tr>
</table>
