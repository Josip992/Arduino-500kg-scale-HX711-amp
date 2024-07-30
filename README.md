# Arduino-500kg-scale-HX711-amp
A FESB Racing (https://ups-fesb.hr/en/) organization assigment i chose where i successfully managed to read motorcycle engine torque from a load cell (up to that point the system was measuring torque/rpm of a car engine).

A HBM Wagezelle (Typ U2A) 500kg  load cell producing milivolt voltage is connected to a Sparkfun SEN-13879 HX711 24-bit analog-to-digital converter (ADC) designed for weight scales/breakout board that amplifies load cells output to a voltage range that Arduino Mega 2560 can read. The loadcell produces 20mV voltage range which is amplified by the HX711 using a default Channel A with a Gain of 128. 

Load cells use a four-wire Wheatstone bridge configuration to connect to the HX711. 
These are commonly colored RED, BLK, WHT, GRN and YLW. Each color corresponds to the conventional color coding of load cells:

Red (Excitation+ or VCC)

Black (Excitation- or GND)

White (Amplifier-, Signal- or Output-)

Green (A+, S+ or O+)

Yellow (Shield)

<figure class="wp-block-table"><table><tbody><tr><td><strong>Load Cell</strong></td><td><strong>HX711</strong></td><td><strong>HX711</strong></td><td><strong>Arduino</strong></td></tr><tr><td><span class="rnthl rntcred">Red</span> (E+)</td><td><strong>E+</strong></td><td><strong>GND</strong></td><td><span class="rnthl rntcblack">GND</span></td></tr><tr><td><span class="rnthl rntcblack">Black</span> (E-)</td><td><strong>E-</strong></td><td><strong>DT</strong></td><td><span class="rnthl rntclgray">Pin 2</span></td></tr><tr><td><span class="rnthl rntclgray">White</span> (A-)</td><td><strong>A-</strong></td><td><strong>SCK</strong></td><td><span class="rnthl rntcyellow">Pin 3</span> </td></tr><tr><td><span class="rnthl rntclgreen">Green</span> (A+)</td><td><strong>A+</strong></td><td><strong>VCC</strong></td><td><span class="rnthl rntcred">5V</span></td></tr></tbody></table></figure>


Simplified system wiring diagram that is using Arduino Uno

![Arduino-load-cell-diagram_bb](https://github.com/user-attachments/assets/3d2c5068-b785-41e9-9fe8-3bacad2108ab)


![FH7R58EJ7UR7KPT](https://github.com/user-attachments/assets/54743b6f-7779-458d-b7ba-f9148ddcfe3e)

SparkFun Load Cell Amplifier - HX711 (SEN-13879)


Frontside

![13879-SparkFun_Load_Cell_Amplifier_-_HX711-03](https://github.com/user-attachments/assets/bee9e2e0-7d76-45ec-b589-2f9a9f322a70)

Backside

![13879-SparkFun_Load_Cell_Amplifier_-_HX711-04](https://github.com/user-attachments/assets/d7565dbc-3aa3-42a2-b754-e84b13e0d0f7)

My pictures on-site (wiring has been isolated and improved since taking these pictures, this was the first working version of the new motorcycle engine torque measuring system)

![IMG-20230421-WA0004](https://github.com/user-attachments/assets/eca63f8c-ca85-4b41-b345-af66b14dde8e)

![IMG-20240116-WA0023](https://github.com/user-attachments/assets/52e0eaf1-727c-4856-b01b-19b3be653b7e)

![1722355952293](https://github.com/user-attachments/assets/56d4a7be-759a-4758-ae52-d85eac017844)

Code is using the following library 'https://github.com/bogde/HX711'
