//Libraries
#include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>

//OLED specs
#define SCREEN_WIDTH 128
#define SCREEN_HEIGHT 32
//Declaration for an SSD1306 display connected to I2C (SDA, SCL pins)
Adafruit_SSD1306 display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, -1);

//Relay pin settings
#define relayS 7

//Rotary encoder pin settings
#define rotaryA 8
#define rotaryB 2

//Soil sensor pin settings
#define analogInPin A1

//Variables
int dryValue;
int counter;
int aState;
int aLastState;
int sensorValue;

void setup() {
  pinMode (rotaryA, INPUT);
  pinMode (rotaryB, INPUT);

  pinMode(relayS, OUTPUT);

  Serial.begin(115200);
  
  if (!display.begin(SSD1306_SWITCHCAPVCC, 0x3C)) {
    Serial.println(F("SSD1306 allocation failed"));
    for (;;);
  }
  delay(2000);
  display.setRotation(2);
  display.clearDisplay();
  display.setTextColor(WHITE);

  aLastState = digitalRead(rotaryA);
  attachInterrupt(digitalPinToInterrupt(rotaryB), wetset, CHANGE);
}


void loop() {
  delay(500);
  dryValue = counter;


  //Instantiate the soil sensor
  int t = analogRead(analogInPin) / 10 +12;

  if (isnan(t)) {
    Serial.println("Failed to read soil!");
  }
  Serial.print("soil sensor = " );
  Serial.println(t);



  //Watering trigger loop
  if ( t <= dryValue ) {
    digitalWrite(relayS, HIGH);
    
    
    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering.");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering..");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering...");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering....");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering.....");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering......");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering.......");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering........");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering.........");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering..........");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering...........");
    display.display();

    Serial.print("Soil sensor level: ");
    Serial.println(t);
    delay(500);
    display.clearDisplay();
    display.setTextSize(2);
    display.setCursor(0, 3);
    display.print("Watering............");
    display.display();
    

    digitalWrite(relayS, LOW);
  }


  //Watering trigger loop end


  //Normal display loop
  display.clearDisplay();
  display.setTextSize(2);
  display.setCursor(0, 3);
  display.print("Soil: ");
  display.setTextSize(2);
  display.setCursor(70, 3);
  if ( t >= 100 ) {
    display.print("100%");
  } else {
    display.print(t);
    display.print("%");
  }
  display.setTextSize(1.5);
  display.setCursor(0, 22);
  display.print("Watering trigger: ");
  display.setCursor(109, 22);
  display.print(counter);
  display.print("%");
  display.display();

  delay(1000);

  display.clearDisplay();
  display.setTextSize(2);
  display.setCursor(0, 3);
  display.print("Soil: ");
  display.setTextSize(2);
  display.setCursor(70, 3);
  if ( t >= 100 ) {
    display.print("100%");
  } else {
    display.print(t);
    display.print("%");
  }
  display.setTextSize(1.5);
  display.setCursor(0, 22);
  display.print("Watering trigger: ");
  display.setCursor(109, 22);
  display.print(counter);
  display.print("%");
  display.display();

  delay(1000);

  display.clearDisplay();
  display.setTextSize(2);
  display.setCursor(0, 3);
  display.print("Soil: ");
  display.setTextSize(2);
  display.setCursor(70, 3);
  if ( t >= 100 ) {
    display.print("100%");
  } else {
    display.print(t);
    display.print("%");
  }
  display.setTextSize(1.5);
  display.setCursor(0, 22);
  display.print("Watering trigger: ");
  display.setCursor(109, 22);
  display.print(counter);
  display.print("%");
  display.display();

  delay(1000);

}


//Wetset interrupt loop to set the 'counter' variable for the watering trigger
void wetset() {
  {
  volatile static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 3 )  // ignores interupts for 3 milliseconds
  {
    aState = digitalRead(rotaryA);
  if (aState != aLastState) {
    if (digitalRead(rotaryB) != aState) {
      if (counter >= 1) {
        counter --;
      }
    } else {
      if (counter <= 99) {

        counter ++;
      }
    }
    Serial.print("Watering trigger: ");
    Serial.println(counter);
  }
  aLastState = aState;
  }
  last_interrupt_time = interrupt_time;
}
}
