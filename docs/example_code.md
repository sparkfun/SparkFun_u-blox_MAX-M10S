We're just going to look at example two (i.e. "**Example2_NMEAParsing.ino**") which in my opinion, makes it clear the awesomeness of these GPS receivers. That is to say, talking to satellites and finding out where in the world you are.     

    language:c
    #include <Wire.h> //Needed for I2C to GPS

    #include "SparkFun_u-blox_GNSS_Arduino_Library.h" //Click here to get the library: http://librarymanager/All#SparkFun_u-blox_GNSS
    SFE_UBLOX_GNSS myGNSS;

    void setup()
    {
      Serial.begin(115200);
      Serial.println("SparkFun u-blox Example");

      Wire.begin();

      if (myGNSS.begin() == false)
      {
        Serial.println(F("u-blox GNSS module not detected at default I2C address. Please check wiring. Freezing."));
        while (1);
      }

      //This will pipe all NMEA sentences to the serial port so we can see them
      myGNSS.setNMEAOutputPort(Serial);
    }

    void loop()
    {
      myGNSS.checkUblox(); //See if new data is available. Process bytes as they come in.

      delay(250); //Don't pound too hard on the I2C bus
    }

When you upload this code you'll have to wait ~24s to get a lock onto any satellites. After that first lock, the backup battery on the board will provide power to some internal systems that will allow for a **hot start** the next time you turn on the board. The **hot start** only lasts four hours, but allows you to get a lock within one second. After you get a lock the [serial terminal](https://learn.sparkfun.com/tutorials/terminal-basics/arduino-serial-monitor-windows-mac-linux) will start listing longitude and latitude coordinates, as seen below. Make sure to set the serial monitor to **115200 baud**.

<span style="display:block;text-align:center"> [![This image shows a screenshot of the Arduino Serial terminal spitting out latitude and longitude data.](https://cdn.sparkfun.com/assets/learn_tutorials/8/6/9/nmeaCapture-ublox2.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/8/6/9/nmeaCapture-ublox2.jpg) </span>

<span style="display:block;text-align:center"> _These are the coordinates for SparkFun HQ_ </span>
