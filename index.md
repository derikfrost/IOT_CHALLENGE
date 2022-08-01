# Kerala IoT Challenge 

> **Foxlab Makerspace** in association with **GTech - Group of Technology Companies** in Kerala is launching our prestigious program  **“Kerala IoT Challenge 2021”**,  with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

# IOT_Level_1
level one experiments

## experiment 1
### LED Blinking
Components Required
1. Arduino Uno Board
2. USB Cable
3. LED(Any Color)x 1
4. 220 OHM res x 1
5. Breadboard
6. Jumper Wires(Male to Male)x 2

code

```arduino

int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}
```
Result
<iframe width="560" height="315" src="https://www.youtube.com/embed/aad3VFreHxM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



***

## Experiment 2
### Traffic Light

components required
1. Arudino board 
2. USB cable 
3. Red M5 LED 
4. Yellow M5 LED
5. Green M5 LED
6. 220 ohm resistor
7. breadboard 
8. breadboard jumper wires

Circuit Diagram


![yiU1x_3102_1627566759](https://user-images.githubusercontent.com/77291059/131890696-16337309-ce81-4ffc-b089-3bbafa9cb33f.png)

code
```arudino
int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}
```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/vWrNEMp6SrY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


---
## Experiment 3
### LED Chasing Effect

components required 
1. LED *6
2. Arduino board 
3. 220 ohm resistor*6
4. usb cable*1
5. jumper cables*13

circuit

![s5yR0_3102_1627567167](https://user-images.githubusercontent.com/77291059/131891349-af18ed63-edd5-4e3b-96c5-527695843a58.png)

code 

```arduino
int BASE =2;  // the I/O pin for the first LED
int NUM =6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}
```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/qvoKrumxAIk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


---
## Experiment 4
### Button Controlled LED


components required

1. Arduino uno
2. button switch *1
3. Red M5 LED *1
4. 220 ohm Resistor *1
5. 10kohm Reisitor *
6. Breadboard *1
7. USB cable *1


Circuit Diagram

![Ztk6E_3102_1628160172](https://user-images.githubusercontent.com/77291059/131892651-faa050c3-0c7e-467d-888a-8f4e5bc933a7.png)


```arduino
int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}
```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/NFxV2qFHjZs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


---
## Experiment 5
### Buzzer

Components Required

1. Arduino Uno
2. buzzer *1
3. breadboard *1
4. breadboard jumper wire*2
5. usb cable*1


Circuit Diagram


```arduino
int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}
```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/26S82Y2klrE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


***
## Experiment 6
### RGB LED

Components Required 

1. Arduino Uno
2. USB Cable *1
3. RGB LED *1
4. resistor (220 ohm) *3
5. Breadboard Jumper Wire*5


Circuit Diagrm

![xX9cw_3102_1628160649](https://user-images.githubusercontent.com/77291059/131893555-571b8892-4695-47df-b871-87c8e346c1b0.png)


Code

```arduino

int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=500; val>0; val--)
  {
  ```
  ***
  ## Experiment 7
  ### LDR Light sensor
  
  Components Reuired 
  1. Arduino Uno 
  2. LDR module *1
  3. red M5 LED *1
  4. 220ohm resistor *1
  5. Jumper Wires
  6. USB cable

circuit 


Code

```arduino
const int ldr_pin = 7;
const int led_pin = 13;
void setup() {
  // put your setup code here, to run once:
    pinMode(ldr_pin,INPUT);
    pinMode(led_pin,OUTPUT);
    Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:
   if( digitalRead( ldr_pin ) == 1){
      digitalWrite( led_pin,HIGH);
   }
   else{
      digitalWrite( led_pin , LOW);
   }
   
   Serial.println( digitalRead( ldr_pin ));
   delay(100);
   }}
   ```
   
   Result
   
   <iframe width="560" height="315" src="https://www.youtube.com/embed/lg68d2hGDpM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
   
   
   ***
   
   ## EXperiment 8
   ### Flame Sensor
   
   Components Required
   1. Arduino Uno Board*1
   2. Flame Sensor(IR reciver)*1
   3. Buzzer*1
   4. 10k Resistor*1
   5. Breadboard Jumper Wire*6
   6. USB cable*1
   
   Circuit Diagram
   ![8GIDe_3102_1628756760](https://user-images.githubusercontent.com/77291059/132124335-aa465be4-7cb2-49af-8ee3-523a90596306.png)
   
   Code
   
   ```arduino
int flame=0;// select analog pin 0 for the sensor
int Beep=9;// select digital pin 9 for the buzzer
int val=0;// initialize variable
 void setup() 
{
  pinMode(Beep,OUTPUT);// set LED pin as “output”
 pinMode(flame,INPUT);// set buzzer pin as “input”
 Serial.begin(9600);// set baud rate at “9600”
 } 
void loop() 
{ 
  val=analogRead(flame);// read the analog value of the sensor 
  Serial.println(val);// output and display the analog value
  if(val>=600)// when the analog value is larger than 600, the buzzer will buzz
  {  
   digitalWrite(Beep,HIGH); 
   }else 
   {  
     digitalWrite(Beep,LOW); 
    }
   delay(500); 
}
```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/D5oHJKS3cOo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***
## Experiment 9
### LM35 Temprature sensor

![3ZHjl_3102_1628757013](https://user-images.githubusercontent.com/77291059/132124422-7925b74f-6bc2-4e0c-83fd-a887d54742f3.png)

 LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing.

LM35 temperature sensor can produce different voltage by different temperature
When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.
The output temperature is 0℃～100℃, the conversion formula is as follows:
![5Bfla_3102_1628757124](https://user-images.githubusercontent.com/77291059/132124443-a4d2db4b-fc6c-45a2-8509-aa27d84a8e13.png)

Components Required

1. Arduino Uno Board*1
2. LM35*1
3. Breadboard*1
4. USB cable*1

Circuit Diagram
![XwF5M_3102_1628757263](https://user-images.githubusercontent.com/77291059/132124492-23b45b25-9d8a-482c-99f8-752a0e9fff09.png)

Code
```arduino
 int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}
```
Result
![lm35](https://user-images.githubusercontent.com/77291059/132124535-40b69bae-1a76-4db1-ab5a-a94753dbf0c8.png)
Serial Monitor Output


***
## Experiment 10
### IR Remote Control Using TSOP

![TSOP1738-Pin-Configuration](https://user-images.githubusercontent.com/77291059/132124625-7cc0e2d1-6590-401d-916d-097bd91dc605.png)
pin diagram

** What is an infrared receiver?**
 The signal from the infrared remote controller is a series of binary pulse code. To avoid the other infrared signal interference during the wireless transmission, the signal is pre-modulated at a specific carrier frequency and then send out by an infrared emission diode. The infrared receiving device needs to filter out other waves and receive signals at that specific frequency and to modulate it back to binary pulse code, known as demodulation.

** Working Principle**
 The built-in receiver converts the light signal it received from the sender into feeble electrical signal. The signal will be amplified by the IC amplifier. After automatic gain control, band-pass filtering, demodulation, wave shaping, it returns to the original code. The code is then input to the code identification circuit by the receiver's signal output pin.
 
 


Components Required

1. Infrared Remote Controller(You can use TV Remote or any other remote) *1
2. Infrared Receiver *1
3. LED *3
4. 220ΩResistor *3
5. Breadboard Wire *11
6. USB cable*1

Circuit Diagram
![0AesB_3102_1629369832](https://user-images.githubusercontent.com/77291059/132124762-6a958e10-e01e-43b2-add0-0ef739ff107d.png)

Code
```arduino
#include <IRremote.h>
int RECV_PIN = 11;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;

long on1  = 0x40BF7A85;
long off1 = 0x40BFBA45;
long on2 = 0x40BF7887;
long off2 = 0x40BF52AD;
long on3 = 0x40BF926D;
long off3 = 0x40BF50AF;

IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if ((i % 2) >= 1) {
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on =0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
         on =  ! on;
//        digitalWrite(8, on ? HIGH : LOW);
        digitalWrite(13, on ? HIGH: LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);
        
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}

```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/dOSDX-LPAYk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***

## Experiment 11
### Potentiometer analog Value Reading

Components Required
1. Arduino Uno Board*1
2. 10K Potentiometer *1
3. Breadboard*1
4. Breadboard Jumper Wire*3
5. USB cable*1

Circuit Diagram
![s0EY9_3102_1629370792](https://user-images.githubusercontent.com/77291059/132124847-071e1ecf-713e-4b5c-88c3-a39ddaaf3acc.png)

Code
```arduino
int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}
```
**Result**

<iframe width="560" height="315" src="https://www.youtube.com/embed/Jbzz3Oq8t-A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***
## Experiment 12
### 7 Segment Display
![buaPu_3102_1629370988](https://user-images.githubusercontent.com/77291059/132124911-1d23e648-7b1e-415c-ab2e-1f957ced6190.png)

LED segment display is a semiconductor light-emitting device. Its basic unit is a light-emitting diode (LED). LED segment display can be divided into 7-segment display and 8-segment display according to the number of segments. 8-segment display has one more LED unit ( for decimal point display) than 7-segment one.

Components Required
1. Arduino Uno Board*1
2. 1-digit LED Segment Display*1
3. 220Ω Resistor*8
4. Breadboard*1
5. Breadboard Jumper Wires *several
6. USB cable*1

Circuit Diagram

Code
```arduino
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}}
```
Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/fpsjQ7hmxh4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***

## Assignments
### Assignment 2

Digital Dice Using 7 Segment Display and Push Button

Components Required 

1. Arduino Uno Board*1
2. 1-digit LED Segment Display(common cathode)*1
3. 220Ω Resistor*6
4. Breadboard*1
5. Breadboard Jumper Wires *several
6. USB cable*1
7. Push button*1
8. 10k resistor*1


Circuit Diagram

![7seg](https://user-images.githubusercontent.com/77291059/132133597-b6fad7f8-64e7-401d-aea4-095746c932fb.png)

Code

```arduino
int f = 5;
int g = 6;
int e = 7;
int d = 8;
int c = 9;
int b = 11;
int a = 12;  //7 Segment pin

int buttonPin=13;
int buttonState=0;
int state=0;
  

void setup() {

  pinMode(f, OUTPUT);
  pinMode(g, OUTPUT);
  pinMode(e, OUTPUT);
  pinMode(d, OUTPUT);
  pinMode(c, OUTPUT);
  pinMode(b, OUTPUT);
  pinMode(a, OUTPUT);
  pinMode(buttonPin,INPUT);

}

void loop() 
{
 buttonState=digitalRead(buttonPin);
 if (buttonState == HIGH){
 state = random(1,7); // take random values from 1 to 6
 switch(state){
 
 case 1:
 digitalWrite(a,0); 
 digitalWrite(b,1);  
 digitalWrite(c,1);  
 digitalWrite(d,0);  
 digitalWrite(e,0);  
 digitalWrite(f,0);  
 digitalWrite(g,0);   // 1
 
 break;
 
 case 2:  
 digitalWrite(a,1); 
 digitalWrite(b,1);  
 digitalWrite(c,0);  
 digitalWrite(d,1);  
 digitalWrite(e,1);  
 digitalWrite(f,0);  
 digitalWrite(g,1);   // 2

 break;
 
 case 3:
 digitalWrite(a,1); 
 digitalWrite(b,1);  
 digitalWrite(c,1);  
 digitalWrite(d,1);  
 digitalWrite(e,0);  
 digitalWrite(f,0);  
 digitalWrite(g,1);   // 3

 break;
  
case 4: 
 digitalWrite(a,0); 
 digitalWrite(b,1);  
 digitalWrite(c,1);  
 digitalWrite(d,0);  
 digitalWrite(e,0);  
 digitalWrite(f,1);  
 digitalWrite(g,1);   // 4
  
  break;
    
case 5:
 digitalWrite(a,1); 
 digitalWrite(b,0);  
 digitalWrite(c,1);  
 digitalWrite(d,1);  
 digitalWrite(e,0);  
 digitalWrite(f,1);  
 digitalWrite(g,1);   // 5

  break;
  
 case 6: 
 digitalWrite(a,1); 
 digitalWrite(b,0);  
 digitalWrite(c,1);  
 digitalWrite(d,1);  
 digitalWrite(e,1);  
 digitalWrite(f,1);  
 digitalWrite(g,1);   // 6

  break;
 }             
}
}
```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/OEm2LbqdDDI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



***
### Assignment 1

Automatic Night Lamp Model Using LDR and LED

Components Required
1. Arduino Uno Board*1
2. LM35*1
3. Breadboard*1
4. USB cable*1
5. LED(10mm)*3


Code 

```arduino
const int LEDpin = 13;  
const int ldrPin = A0;  


void setup() {

  Serial.begin(9600);
  pinMode(LEDpin, OUTPUT); 
  pinMode(ldrPin, INPUT);   
}

void loop() {

  int ldrStatus = analogRead(ldrPin);  
  

   if (ldrStatus <=400) {

    digitalWrite(LEDpin, LOW);               
    Serial.println("LDR is DARK, LED is ON");
    
   }
  else {

    digitalWrite(LEDpin, HIGH);         
    Serial.println("---------------");
  }
}
```

Result

<iframe width="560" height="315" src="https://www.youtube.com/embed/o9gz5S1LRHQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***

# IOT_LEVEL_2
### Experiment 1 - LED Program Using Blynk App
![EXP1](https://user-images.githubusercontent.com/77291059/144716235-32b8c988-1936-4850-85bd-563747201c6e.png)

#### Components Required:
1. ESP32 board
2. Blynk App & Server account
3. LED bulbs
4. Breadboard

#### Code

```ino
// Fill-in information from your Blynk Template here
#define BLYNK_TEMPLATE_ID "TMPLpemtlV3I"
#define BLYNK_DEVICE_NAME "LED BLINK"

#define BLYNK_FIRMWARE_VERSION        "0.1.0"

#define BLYNK_PRINT Serial
//#define BLYNK_DEBUG

#define APP_DEBUG

// Uncomment your board, or configure a custom board in Settings.h
//#define USE_WROVER_BOARD
//#define USE_TTGO_T7
//#define USE_ESP32C3_DEV_MODULE
//#define USE_ESP32S2_DEV_KIT

#include "BlynkEdgent.h"
BLYNK_WRITE(V0)
{
  int pinValue = param.asInt();
  digitalWrite(15,pinValue);
}

void setup()
{
  pinMode(15,OUTPUT);
  Serial.begin(115200);
  delay(100);

  BlynkEdgent.begin();
}

void loop() {
  BlynkEdgent.run();
}
```
The code is a part derived from a library package for setting up the blynk server.

#### Output

<iframe width="560" height="315" src="https://www.youtube.com/embed/e4vzXtK563w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***

### Experiment 2 - IoT Remote Light Meter using Arduino IoT Cloud

#### Components Reequired:

1. ESP32 board
2. ldr light sensor
3. Arduino IoT cloud account
4. Breadboard

#### Code

```ino
/* 
  Sketch generated by the Arduino IoT Cloud Thing "Untitled"
  https://create.arduino.cc/cloud/things/2e068bb5-80f9-4c38-aa96-5e36b74c0b1a 

  Arduino IoT Cloud Variables description

  The following variables are automatically generated and updated when changes are made to the Thing

  CloudLight led;
  float sensor;

  Variables which are marked as READ/WRITE in the Cloud Thing will also have functions
  which are called when their values are changed from the Dashboard.
  These functions are generated with the Thing and added at the end of this sketch.
*/

#include "thingProperties.h"

void setup() {
  // Initialize serial and wait for port to open:
  pinMode(2,OUTPUT);
  pinMode(34,INPUT);
  Serial.begin(9600);
  // This delay gives the chance to wait for a Serial Monitor without blocking if none is found
  delay(1500); 

  // Defined in thingProperties.h
  initProperties();

  // Connect to Arduino IoT Cloud
  ArduinoCloud.begin(ArduinoIoTPreferredConnection);
  
  /*
     The following function allows you to obtain more information
     related to the state of network and IoT Cloud connection and errors
     the higher number the more granular information you’ll get.
     The default is 0 (only errors).
     Maximum is 4
 */
  setDebugMessageLevel(2);
  ArduinoCloud.printDebugInfo();
}

void loop() {
  ArduinoCloud.update();
  float val = analogRead(34);
  sensor = val;
 }

/*
  Since Led is READ_WRITE variable, onLedChange() is
  executed every time a new value is received from IoT Cloud.
*/
void onLedChange()  {
  // Add your code here to act upon Led change
  
  if(led==HIGH)
  {
    digitalWrite(2,HIGH);
  }
  else
  {
    digitalWrite(2,LOW);
  }
  ```
  #### Circuit Diagram
  
![exp2](https://user-images.githubusercontent.com/77291059/144716565-d11197af-1f1c-47fb-beba-9ec30f1cfc0e.jpg)

#### Output

<iframe width="560" height="315" src="https://www.youtube.com/embed/nIyIVTJNvXs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***
### Experiment 3 - Soil Moisture Meter

![iqLj2_3102_1634392140](https://user-images.githubusercontent.com/77291059/144716647-921f4ca5-7124-4f6a-ba03-d7aa3dcb536f.png)

#### Components Reequired:
1. ESP32 board
2. soil moisture sensor
3. Arduino IOT cloud account
4. breadboard


> **Note: Experiment 2 and 3 have the same components and code except for the change in sensor.**

#### Circuit Diagram

![whDtU_3102_1634392072](https://user-images.githubusercontent.com/77291059/144716723-bacc23b8-9d74-4478-b7d6-8ae43a4d9707.png)
![Ik0yW_3102_1634392236](https://user-images.githubusercontent.com/77291059/144716731-51c52221-e6a5-42bd-aeac-4e5cfa0caa55.jpg)


#### Output

<iframe width="560" height="315" src="https://www.youtube.com/embed/w3s9WQ6HZCo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Experiment 4 - Ultrasonic Sensor
![4 UltrasS](https://user-images.githubusercontent.com/67751535/140392891-458fb08a-ed90-4c28-a5df-4d73ec1af47b.jpg)

#### Components Required:

1. HC-SR04 Ultrasonic Sensor
2. ESP32 board
3. Breadboard
4. Jumper wires

#### Code

```ino
const int trigPin = 5;
const int echoPin = 18;

//define sound speed in cm/uS
#define SOUND_SPEED 0.034
#define CM_TO_INCH 0.393701

long duration;
float distanceCm;
float distanceInch;

void setup() {
  Serial.begin(115200); // Starts the serial communication
  pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output
  pinMode(echoPin, INPUT); // Sets the echoPin as an Input
}

void loop() {
  // Clears the trigPin
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  // Sets the trigPin on HIGH state for 10 micro seconds
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  
  // Reads the echoPin, returns the sound wave travel time in microseconds
  duration = pulseIn(echoPin, HIGH);
  
  // Calculate the distance
  distanceCm = duration * SOUND_SPEED/2;
  
  // Convert to inches
  distanceInch = distanceCm * CM_TO_INCH;
  
  // Prints the distance in the Serial Monitor
  Serial.print("Distance (cm): ");
  Serial.println(distanceCm);
  Serial.print("Distance (inch): ");
  Serial.println(distanceInch);
  
  delay(1000);
}
```
#### Circuit Diagram

![4](https://user-images.githubusercontent.com/67751535/140394451-b623f6cc-7ebd-408c-ac85-af1a6a869fcd.png)

#### Output

<iframe width="560" height="315" src="https://www.youtube.com/embed/Snsfey0ky7c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Experiment 5 - Object Detection using IR Sensor

![5 Ir](https://user-images.githubusercontent.com/67751535/140392118-9b45b197-d6e7-467f-a8a2-2f0c3e5bde06.jpg)

#### Components Required:
1. ESP32 board
2. IR sensor
3. Arduino IOT cloud account
4. Breadboard

#### Circuit Diagram:

![5](https://user-images.githubusercontent.com/67751535/140394502-cecde79b-c28c-4c1b-aed7-f1e1fedc8f7e.png)

#### Output

<iframe width="560" height="315" src="https://www.youtube.com/embed/9P-yxpnInj0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***

### Experiment 6 -MIT App Inventor + ESP8266

![1shHv_3102_1641460068](https://user-images.githubusercontent.com/77291059/182179316-7b77ae4c-c024-46fb-aafb-09682d303061.png)

#### What is MIT App Inventor
MIT App Inventor is a web application integrated development environment for creating Mobile Apps originally provided by Google, and now maintained by the Massachusetts Institute of Technology.

#### Components Required
1. ESP8266 board
2. HC-5 Blutooth module
3. Breadboard
4. LED's
5. jumper wires
6. 220Ω Resistor*3

#### code

```ino
// --------------------------------------------------
//
// Code for control of ESP12E and Hc5 module through MIT inventor app (Bluetooth). 
// device used for tests: ESP12E
// 
// App on phone has three buttons:
// Button 1: 11 for ON and 10 for OFF
// Button 2: 21 for ON and 20 for OFF
// Button 3: 31 for ON and 30 for OFF
//
//
//
// --------------------------------------------------





// init PINs: assign any pin on ESP32
int led_pin_1 = 16;
int led_pin_2 = 0;
int led_pin_3 = 2;
     

// Parameters for Bluetooth interface
int incoming;

void setup() {
  Serial.begin(9200);
  

  pinMode (led_pin_1, OUTPUT);
  pinMode (led_pin_2, OUTPUT);
  pinMode (led_pin_3, OUTPUT);
}

void loop() {
  
  // -------------------- Receive Bluetooth signal ----------------------
  if (Serial.available()) 
  {
    incoming = Serial.read(); //Read what we receive 

    // separate button ID from button value -> button ID is 10, 20, 30, etc, value is 1 or 0
    int button = floor(incoming / 10);
    int value = incoming % 10;
    
    switch (button) {
      case 1:  
        Serial.print("Button 1:"); Serial.println(value);
        digitalWrite(led_pin_1, value);
        
        break;
      case 2:  
        Serial.print("Button 2:"); Serial.println(value);
        digitalWrite(led_pin_2, value);
        
        break;
      case 3:  
        Serial.print("Button 3:"); Serial.println(value);
        digitalWrite(led_pin_3, value);
        break;
    }
  }
}
```
#### NOTE
initially the code was designed for ESP32 Wroom module which has blutooth inbuilt, here i'm using an esp8266 module which does not have blutooth. to overcome this I am using HC-5 blutooth module connected to the RX & TX pin of the ESP8266 module, some edit have been doen to the arduino program in order to this work. 


![Bluetooth Interfacing with NoeMCU](https://user-images.githubusercontent.com/77291059/182188997-e09db681-0214-4142-aa6b-ee7d3efbd84e.png)

#### Output

<iframe width="560" height="315" src="https://www.youtube.com/embed/JqY4JAPbeU0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

***


