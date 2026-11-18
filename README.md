# EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO
# AIM:  To interface a Analog  input (angular displacement sensor POT) and scale the values up on change in the input.

# NAME: MURUGA.S

# REG NO: 212225040265

# DEPARTMENT: BE.CSE

# COMPONENTS REQUIRED:

1.      10 KΩPOT

2.      1 KΩ resistor

3.      Arduino Uno

4.      USB Interfacing cable

5.      Connecting wires

6.      LED of choice

# Procedure:

1. Open Tinkercad → Circuits and create a new circuit.

2. Drag an Arduino Uno R3 into the workspace.

3. Add a breadboard.

4. Add a potentiometer to the breadboard.

5. Connect one outer pin of the potentiometer to 5V of Arduino.

6. Connect the other outer pin to GND of Arduino.

# Algorithm:

STEP 1 : Start

STEP 2 : Connect the potentiometer to Arduino.

STEP 3 : Connect the potentiometer's wiper pin to analog pin A0.

STEP 4 : Initialize serial communication.

STEP 5 : Read the analog voltage from A0 using analogRead().

STEP 6 : Store the value in a variable.

STEP 7 : Display the value on the Serial Monitor.

STEP 8 : Rotate the potentiometer and observe the change in value.

STEP 9 : Repeat steps 5–8 continuously.

# PROGRAM:

```
const int sensorPin=A0;
const int ledPin=9;
void setup(){
  pinMode(ledPin, OUTPUT);
    Serial.begin(9600);
}

  void loop() {
   int sensorValue = analogRead(sensorPin);
  
  
  int brightness = map(sensorValue, 0, 1023, 0, 255);
  
  analogWrite(ledPin, brightness);
  
  
  Serial.print("Sensor: ");
  Serial.print(sensorValue);
  Serial.print(" -> LED Brightness: ");
  Serial.println(brightness);
  
  delay(10);
}
```

# OUTPUT:

LED OFF:

<img width="1112" height="750" alt="image" src="https://github.com/user-attachments/assets/a9275190-b14d-4f63-84c3-399834e82fbe" />

LED ON:

<img width="832" height="738" alt="image" src="https://github.com/user-attachments/assets/3f49d963-8670-413c-96d3-3898fa225474" />

# RESULT:

Thus a Analog input (angular displacement sensor POT) and scale the values up on change in the input has been executed successfully.
