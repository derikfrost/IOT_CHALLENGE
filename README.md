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
