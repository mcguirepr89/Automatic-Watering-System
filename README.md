
# Automatic-Watering-System
This is just a cool little automated watering system that I made for my friend, Jerry Vance. He's the inspiration behind this thought and design and the motivation to get it done.

The hardware consists of the following, in what I consider the order of imporatance:

  Arduino Nano
  OLED SSD 1306 Display
  5v Relay Swith
  Rotary Encoder
  5v Water Pump
  Soil Sensor
  mounted on a PCB for convenience

The "soil sensor" is not a module, but just a set of probes, one of which has paths to the A1 analog pin and another with 10K Ohms resistance to ground. The other probe is hooked up to the +5v pin.

The Relay IS a module, and has it's signal pin hooked up to the D7 digital pin.
The Rotary Encoder has the A and B pins hooked up to the D8 digital and D2 digital pins, respectively. The C and E pins are grounded. The rotary encoder's D pin, that can be used of the encoder's push button signal, is not in use for this project, though I'm sure there is something cool that can be done for it.

The OLED uses IC2 connection to be read by the microcontroller, so it is using the A4 analog pin for it's data and the A5 pin for the clock.

THAT'S IT! Everything that is needed to get this going is in the code and should be commented accordingly.
