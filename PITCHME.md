## Sensing the world around you
sensors and what they do
---
## What is a sensor?
A sensor is an electronic device that can transform a physical property of our world into an electrical signal that a computer can understand.

The only thing that you need to know about a sensor for now is that it is "a value that moves through time". People in finance call that a "ticker" in EE it's called a "signal" in electronic music they call it a "control signal" but in all of them they mean "a value that moves through time".
---
## There are (for now) two types of sensors
We can classify them according to the kind of signal that they produce: (and let's imagine a hypothetical sensor for dog poop)
  - digital (two states)
    - poop happened (HIGH = 1)
    - poop didn't happen (LOW = 0)
  - analog
    - how much of the actual poop happened
    - it is often a number between 0 and 1024
---
### Light-level sensor
setup your breadboard
![LDR sensor](http://res.cloudinary.com/zilogtastic/image/upload/c_scale,h_450/v1506369513/ldr_arduino_ppac8t.jpg)
---
### code
###### reading the LDR sensor with Arduino
```
void setup() {
  Serial.begin(9600);
  pinMode(A0, INPUT); // let the computer gods know that we shall use A0 as our sensor input pin
}

void loop() {
  int value = analogRead(A0);   // read the sensor value on pin A0
  Serial.println(value);
  delay(20);        // this delay determines the "sampling rate"
}
```
---
## CHOOSING A SENSOR
there are many different kinds of sensors, and the field is expanding constantly, here's a brief selection of the most commonly used sensors
---
### Distance
- [Ultrasonic rangefinder](https://www.google.com/search?q=Ultrasonic+sensor)
- [IR sensor](https://www.google.com/search?q=IR+sensor)
### Presence & motion
- [PIR sensor](https://www.google.com/search?q=PIR+sensor) (passive infrared)
---
### Smoke, gas and alcohol
- [MQ-2 smoke sensor](https://www.google.com/search?q=MQ-2+smoke+sensor)
- [MQ-3 Alcohol-ethanol (breathalyzer)](https://www.google.com/search?q=MQ-3+smoke+sensor)
---
### Touch
- Button
- Switch
- [Potentiometer](https://www.google.com/search?q=potentiometer)
- Capacitive sensing
  - simple resistor circuit (see cap. sensing slides)
  - [QT113](https://www.google.com/search?q=QT113+sensor)
---
### Movement
- Tilt sensor
- Vibration sensor
- Joystick
---
### Acceleration
- Accelerometer
- Gyroscope
- IMU (Inertial motion unit, 9-DoF)
---
IMU-based motion capture and digital scenography
![YCAM Awareness in Motion](https://player.vimeo.com/video/61942488)
---
### Light
- LDR (light dependent resistor)
- Flame sensor
- UV index sensor
- Color sensor (RGB)
- Camera (3CCD)
- Thermal camera
---
### Weather
- Barometric pressure
- Wind (anemometer)
- Temperature
- Soil humidity
- Atmospheric humidity
---
[James Bridle's A Ship Adrift](https://jamesbridle.com/works/a-ship-adrift)
where he installed a weather station on top of the Southbank Centre in London and used the data generated, including wind speed and air pressure, to determine the path of an "imaginary mad airship". The program logs its theoretical position on Google Maps and gathers streams of information from the internet that are tagged with that location, using them to generate tweets and a log that combine a selection of words it picks up. [from Dezeen](https://www.dezeen.com/2012/10/02/the-internet-has-escaped-out-into-the-street-says-james-bridle/)
---
Weather thingy by Adrian Kaeser
![Weather thingy](https://player.vimeo.com/video/292088058)
---
### Identity
- [Fingerprint scanner](https://www.google.com/search?q=fingerprint+sensor)
- RFID/NFC
- Keypad
---
### Electricity and magnetism
- Magnetometer
- Hall effect sensor (magnetic fields)
- Compass
- Solar cell
---
### Sound
- Microphone
- Clap sensor
---
### Biosignals
Are kinds of signals that can be (continually) measured and monitored from biological beings. The term biosignal is often used to mean bio-electrical signal but in fact, biosignal refers to both electrical and non-electrical signals.
---
### Biosignals
measuring electrical potentials (aka electrophysiology)
- [EEG (electroencephalogram)](https://www.google.com/search?&q=EEG)
- EKG/ECG (electrocardiogram) 
- EMG (electromyography)
- Respiration
- Goniometer (position / angle)
- GSR (galvanic skin response, aka EDA electro dermal activity)
---
### Biosignals
non-electrical signals (e.g. acustic)
- Breathing rhythm (lungs)
- Pulse oxymeter (pulse / light) aka [PPG photoplethysmography](https://www.google.com/search?q=ppg+sensor&source=lnms&tbm=isch&sa=X&ved=0ahUKEwjg2vSDo8TeAhWtPOwKHZF2AtoQ_AUIDigB&biw=1099&bih=612)
- Muscles (Xth sense)
- Esthetoscope (sound)
- Ultrasound (baby's heart monitor)
- Heart
- Gut
---
For medical applications electrophysiology is more widely used, but acoustic methods can be more
effective in other contexts, such as dealing with phobic reactions for example.
---
Marco Donnarumma scholar, inventor, performer and artist. Developed the Xth Sense, a music instrument that uses the acoustic signals of the artist's muscles and processes them using sound design tools to produce synthesized music
![Marco Donnarumma](https://player.vimeo.com/video/130620543)
---
Hypo Chrysos by Marco Donnarumma
![Hypochrysos](https://player.vimeo.com/video/37921373)
---
Most biosignals are either electrically weak or acoustically weak and they all are fairly complex, so they require heavy amplification, are prone to noise and require extensive digital signal processing (DSP) before they can be used.
---
### Example QRS complex
![QRS complex](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/QRS_complex.png/220px-QRS_complex.png)
---
Biofeedback is the process of giving the user stimuli that are synchronized to biosignals. The user is instrumented with some kind of measurement device that provide activity on a biological function of the user and a stimulus is generated from that signal that is then fed back to the user. It is a technique to train users to gain greater control of the physiological functions of their bodies. Some meditation apps use this principle to enable people to gain greater control over their minds.
---
### Brain activity
- [MUSE headband](https://choosemuse.com/)
- [Emotiv headset](https://www.emotiv.com/)
- [HOLST Centre](https://www.google.com/search?q=holst+centre+EEG+headset)
---
- [EEG kiss sketch](https://player.vimeo.com/video/113102248)
- [EEG kiss theatrical setup](https://player.vimeo.com/video/158300331)
---
### Biosensing platforms
- [BITalino](http://bitalino.com/en/)
- [BITalino sensor kit](http://biosignalsplux.com/en/products/sensors)