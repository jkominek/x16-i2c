Rough draft of an I2C expansion card for the [Commander X16](https://www.commanderx16.com/)

I don't have any real hardware, and haven't fabbed this. So there's little reason to believe it works.

* Features
  * PCA9548A I2C eight port multiplexer, so you can use a lot of I2C devices without loading the bus down. Also lets you use multiple identical devices, which would otherwise have conflicting addresses.
  * Four I2C ports are brought out [SparkFun Qwiic](https://www.sparkfun.com/qwiic)-style, with 3.3V power.
    * Why that connector? Sparkfun has a lot of Qwiic hardware, and Adafruit as a bunch of [STEMMA QT](https://www.adafruit.com/category/1018) hardware, which is compatible. Some other companies have some similar products. This gets you dozens of compatible IO devices in one fell swoop.
  * Three are headers on the board, with 5V power, for use "inside the case"
  * Last port is on a PCA9615 differential I2C transceiver, for very distant I2C devices.
    * It provides 3.3V and 12V.
    * Intended to be compatible with the [Sparkfun QwiicBus Endpoint](https://www.sparkfun.com/products/16988)
  * One mandatory 3.3V regulator for the external I2C ports.
  * You can add one or two other additional regulators, to provide more power to your I2C devices.

I'll revisit and revise this as more docs come out, and whenever I get real hardware.
