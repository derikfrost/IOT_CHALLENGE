# IOT_L1
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


---
## Experiment 3
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
   ```
   ****
   
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
3. LED *6
4. 220ΩResistor *6
5. Breadboard Wire *11
6. USB cable*1

Circuit Diagram
![0AesB_3102_1629369832](https://user-images.githubusercontent.com/77291059/132124762-6a958e10-e01e-43b2-add0-0ef739ff107d.png)

Code
```arduino

```

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






