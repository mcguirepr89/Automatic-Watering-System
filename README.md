# Automatic-Watering-System

This project was inspired by and made for my best friend, Jerry Vance. He's the inspiration, generation, and motivation to get this done. Many thanks to Susan Mackey for her help in making this possible.

The basic idea is that there is a homemade "soil sensor" that reads a soil water-saturation level out of about 1000. I have devided that by 10, put it as a percentage out of 100, created a variable that can be set within that 0-100 range at which time a water pump will be powered on and will water the plant whose soil the sensor reads.

The hardware:

  OLED Display
  5v Relay Switch (module)
  5v Water Pump
  Rotary Encoder (no module)
  Soil Sensor (no module)
  
The OLED is defined as I2C, so the data and clock are connected to the A4 and A5 analog pins, respectively.
The Relay's signal is read from the D7 digital pin.
The Rotary Encorder's A and B pins are hooked up to the D8 and D2 digital pins, respectively. The C and E pins are grounded and the D pin is not in use (it controls the push button switch portion of the encoder).

THAT'S IT! The rest of the work is either in the code or in setting the trigger via the rotary encoder.
