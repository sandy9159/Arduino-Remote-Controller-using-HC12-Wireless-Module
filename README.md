# Arduino-Remote-Controller-using-HC12-Wireless-Module

![image](https://user-images.githubusercontent.com/19898602/159052217-23807555-2f6b-4b67-bb45-47d1470b664f.png)


I will give you the complete schematics, codes and complete layout of all the boards used in this Arduino RC robot to make one yourself. So stay tuned!



# 6-Wheel Drive Rough Terrain Robot Chassis

The whole off-road robot chassis is built using 2 mm aluminum alloy and the surface is coated with aluminum.

Even though the material is lightweight, it is very strong and can carry all the; components - microcontroller, sensors and motors without any hassle.

![image](https://user-images.githubusercontent.com/19898602/158980425-52e0829c-d76f-4b41-a628-ccb0f8cdcc62.png)

It has 6 high-speed DC motors, with an RPM of 17, 000 combined with 1:34 full metal gearbox, enabling your 6-wheeled robot to obtain amazing speed and off-road performance. The use of six hydraulic spring dampers ensure adaptive driving experience even on rough terrains and uneven surfaces.

# Arduino Off-Road Robot Components
Robot Chassis

> Arduino Pro Mini

> HC12

> Remote Controller

> VNH2SP30 Motor Driver

> LiPo Battery

# Making Arduino RC Robot

![image](https://user-images.githubusercontent.com/19898602/158980642-a3dc6b6b-b469-483a-8acc-963d8e491203.png)


# HC12

Here, we will be using HC 12 wireless module for transmitting data from the DIY Remote Controller to the RC Robot. 

They are commonly used in remote controlled robots and other wireless communication projects. This wireless module works under 433 megahertz frequency. 

When combined with an external antenna, this wireless module can transmit and receive data from a distance 

of up to 1 Kilometer line of sight and due to this reason we will be using this wireless module for our robot.


![image](https://user-images.githubusercontent.com/19898602/158980747-bb3ef84b-35a6-4ef9-a1ae-c8ee2286ff83.png)


This wireless module can be easily connected to arduino or Raspberry Pi, and start using it for your project right away. 

Another advantage of using HC12 wireless module for your RC robot is, this module requires only two pins – TX and RX, for data transfer. 

You can save the rest of the pins of your arduino or Raspberry Pi for other things.

# High current Motor Driver

As I mentioned earlier this robot chassis have 6 high speed DC Motors with a speed of 17000 RPM combined with 1:34 metal gear box. 

Each motor draws a current of about 350 milli ampere. As you might know, for almost all of my Robots, I use either L293D motor driver or L298N motor driver.

Here also I tried L293D and L298N Piggybacked. Even though it worked fine, too much energy was wasted as heat after 5 minutes of continuous usage.

![image](https://user-images.githubusercontent.com/19898602/158980885-2261b54b-df27-4b56-a4c2-e624f42facea.png)


So I decided to go for another high current motor driver, named VNH2SP30, that can provide a peak current of 30 amperes.

If you are not familiar with this VNH2SP30 High Current DC Motor Driver, please click this link you know more about it.

This motor driver board can control only one motor at a time. So here we will be using two motor driver boards to control both DC motors.


# Powering up the Off Road Robot

For this project I’ll be using a 12 volt Lithium polymer battery as a power source. 

This can provide enough power to drive all the six DC Motors, power up the arduino, HC12 module and the motor drivers without any issues.

![image](https://user-images.githubusercontent.com/19898602/158980991-0c509a6a-11db-41aa-a78a-5d11246152b0.png)


That's all you need to know about all the components used in this off road RC robot. started with making the robot.

Want to make one yourself? Complete code and circuit are available Arduino RC Robot

# Arduino Remote Controlled Robot – The Remote controller

![image](https://user-images.githubusercontent.com/19898602/158981103-49b4fa7c-5a7a-4b16-b219-d622d0ba0142.png)

Basically what this remote controller does is, it reads analog and digital data from sensors such as accelerometer buttons joystick and store them in separate variables. These variables will be combined together to form a single long string and this string will be sent to our robot using the HC12 wireless module.

Circuit

I made a circuit which included all the components: the joystick, accelerometer, arduino nano and hc12 module connected to the GPIO pin of the arduino and assembled it on a breadboard.

![image](https://user-images.githubusercontent.com/19898602/158981183-316f5ce5-9820-472d-9f37-7772287be440.png)


t worked flawlessly but the problem was, the whole board looked really messy with all the jumper wires going here and there. So I decided to go with PCB.

In the PCB version, I added 4 switches which I will be using for the next project.

I also added a 7805 regulator which will help me to provide an input voltage between 7V and 35V so that I can use a 5V USB power supply, 9V battery or even 12 V Lipo battery without any issues. I also added some indicator LEDs that will let me know if something stopped working. You will find the circuit in the link below.

![image](https://user-images.githubusercontent.com/19898602/158982303-2216f4cf-815c-45d3-a95f-989e0c4c7d8c.png)

PCB file : -https://drive.google.com/file/d/0B2Iyu3WauhmCdTVxdWJNODhjV29xSXJSZ1k2WGdYaWtXX1Zn/view?usp=sharing&resourcekey=0-vk370xUTQ4HEMvU-ZNROjQ

If you guys planning to order PCB I will suggest you to go with [JLCPCB.com](https://jlcpcb.com/IAT)

First I was also hesitate to try custom PCB my belief was they are much expensive.

but then I came to know about [JLCPCB.com](https://jlcpcb.com/IAT) and I was totally surprised how low price PCB's are they offering 
not only PCB [JLCPCB.com](https://jlcpcb.com/IAT) is one-stop service from  PCB design and PCB prototype to PCB assembly to PCB enclosures,

SMT Assembly service of [JLCPCB.com](https://jlcpcb.com/IAT) is cherry on top now get your PCB fully assembled and save your time and money
Select components for your PCB from there Parts Library of 200k+ in-stock components
they are offering $27 valued New User coupons  & $24 SMT coupons every month
$8.00 setup fee, and $0.0017  per joint

Now no need to order components separately for you PCB and get free from stress of soldering them on PCB just try PCB SMT assembly service and get you PCB with components pre assembled and ready for the project

For more detials & offers please visit [JLCPCB.com](https://jlcpcb.com/IAT)


![image](https://user-images.githubusercontent.com/19898602/134224512-bea8d1c8-9ebe-448d-bbba-0cbecb42d528.png)![image](https://user-images.githubusercontent.com/19898602/130722585-b5268db1-5f17-428f-ba60-b823140f2a70.png)


After downloading the Garber file you can easily order the PCB

1. Visit [JLCPCB.com](https://jlcpcb.com/IAT) and Sign in / Sign up

2. Click on the QUOTE NOW button.

3 Click on the "Add your Gerber file" button. Then browse and select the Gerber file you have downloaded.

![image](https://user-images.githubusercontent.com/19898602/158983798-c8240d19-3e15-4db9-b0ab-0a5f17377eca.png)



4. Set the required parameter like Quantity, PCB masking color, etc

5. After selecting all the Parameters for PCB click on SAVE TO CART button.

![image](https://user-images.githubusercontent.com/19898602/158983820-51e12d9e-5622-4f24-a560-fdf047e268b3.png)



![image](https://user-images.githubusercontent.com/19898602/158983871-d25b0c4b-edb8-4894-b1bb-e07f1b5227b9.png)

6. Type the Shipping Address.

7. Select the Shipping Method suitable for you.

8. Submit the order and proceed with the payment. You can also track your order from the JLCPCB.com.

My PCBs took 2 days to get manufactured and arrived within a week using the DHL delivery option.

PCBs were well packed and the quality was really good at this affordable price.

![image](https://user-images.githubusercontent.com/19898602/158983899-ab2d93d6-b42f-4347-82ec-d3f78b3986e6.png)


![image](https://user-images.githubusercontent.com/19898602/158983956-0cf1954d-3f38-48ce-988f-04001654b89f.png)


# Coding

Now it’s time to upload the code. This is the code. I will share the link in the description, you can simply copy and paste the code and upload it to your controller.


Basically, what this code do is, it will start a software serial connection at pin 10 and 11 where we connect the Tx and Rx pins of HC12 wireless module. 

Arduino will read the analog voltage of the pins A0 – A4 where we connect the sensor inputs (accelerometer and joystick) and store their values in different variables. 

Then it will create a single long string by combining all the data which will then be send to the Remotely Controlled Robot.

Once you are done uploading, open up the serial monitor.

You will see all the sensor data that is being read by the Arduino as a Single line separated by commas (, ). 

This is how our data will be sent to the Remote Robot.


# The Robot
Now it’s time to receive the data from the remote controller. In the receiving unit, I used an Arduino nano clone and another HC12 as receiver.

![image](https://user-images.githubusercontent.com/19898602/158984885-55c9aaff-f7c3-4665-9c9a-dd7b02fb6fe0.png)


ou can use any motor driver board to drive the motors in the robot. This robot chassis have 6 high speed DC Motors with a speed of 17000 RPM. Each motor draws a current of about 350 milli ampere. As you might know, for almost all of my Robots, I use either L293D motor driver or L298N motor driver.

Since we have 6 DC motors, I decided to go for another high current motor driver, named VNH 2SP30, that can provide a peak current of 30 amperes.

If you are not familiar with this VNH2SP30 High Current DC Motor Driver, please click this link to know more about it.

This motor driver board can control only one motor at a time. So here we will be using two motor driver boards to control all the DC motors. 


# The Circuit

Next step, Connecting all the components together. We will connect the HC12 module to the Arduino, which will process the data coming from the HC12 module of the Remote controller.

Once the data is processed, we will drive the motors using the high current DC motor driver connected to the Arduino. The whole circuit will be powered using the LiPo battery.

Connections for the Circuit of RC Robot

Arduino —— HC12

5 Vout – VCC Arduino


Gnd – Gnd

10 – TX

11 – Rx

Arduino —– Motor Drivers


Pin 12 – Motor Driver 1 In1

Pin 13 – Motor Driver 1 In2

Pin 3 – Motor Driver 1 PWM

Pin 8 – Motor Driver 2 In1

Pin 7 – Motor Driver 2 In2

Pin 5 – Motor Driver 2 PWM

Motor Drivers —– Motor

Motor Driver 1 Out 1 – Motor 1 Terminal 1

Motor Driver 1 Out 2 – Motor 1 Terminal 2

Motor Driver 2 Out 1 – Motor 2 Terminal 1

Motor Driver 2 Out 2 – Motor 2 Terminal 2

Motor + – 12 V

Motor – – 0 V

Vcc – 5 V

Gnd – 0 V



# Arduino Code

~~~

#include <SoftwareSerial.h>
#include <Wire.h>
SoftwareSerial HC12(10, 11);

int x;
int y;
int lr;
int bf;
int sw;

void setup()
{ 
HC12.begin(9600);
Serial.begin(9600);
pinMode(A0, INPUT);
pinMode(A1, INPUT);
pinMode(A2, INPUT);
pinMode(A3, INPUT);
pinMode(A4, INPUT);
pinMode(2, OUTPUT);

}
void loop()
{
digitalWrite(A0,0);
digitalWrite(2, HIGH);
x = analogRead(A0);
y = analogRead(A1);

lr = analogRead(A3);
bf = analogRead(A2);
sw = analogRead(A4);

HC12.print(x);
HC12.print(",");
HC12.print(y);
HC12.print(",");
HC12.print(lr);
HC12.print(",");
HC12.print(br);
HC12.print(",");
HC12.print(sw);
HC12.println("");

delay(100);
}

~~~



