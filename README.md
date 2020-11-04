# Contactless Infrared Thermal Scanner with Camera.

### Here is the description of the whole project.
The contactless infrared thermal scanner is a prototype which is able to scan the body
temperature of a person and click its picture as well. 
## Overview: 
With the infrared sensor it will be able to identify the body temperature of a
person and as the device is camera enabled the image of a person is captured with temperature
annotated. Now here the images will be taken with the temperature recorded and will be sent
to the servers and so that it will be easier to identify the people who've had high temperature.
As in right now because of Covid-19 to stop further prevention the people who have high
temperature are needed to be tracked down and with the images which they already have it will
be easy for the government to track down these people.

## Hardware Description:
• Raspberry Pi
• MLX96014- IR Temperature Sensor
• Hdmi 7 Inch Lcd Capacitive Touchscreen 10point Touch 800 X 480
• Raspberry Pi camera.
• Power Adapter/ Power Bank

## Steps to set up: 

1. Gather all the hardware mentioned above.
2. Now connect the hdmi 7 inch lcd capacitive touchscreen 10point touch 800 x 480
display to the Raspberry Pi 
3. Connect the MLX96014 sensor with Raspberry pi using the GPIO pins of it
4. Now connect the Raspberry Pi camera.
5. After the hardware is set up turn on the raspberry pi and the 7 inch LCD display will
start working.
6. By using the PyMLX90614 0.0.3 which is a Python library for MLX90614 infrared
temperature sensors, using smbus2. Compatible with Python 2 and 3. Now to test if the temperature sensor is working or not first, ensure the device is available on the i2c
bus: 
Here by running the command we can see the at which address the i2c bus is connected.
Within Python, the device can be used like this:

,,,
from smbus2 import SMBus
from mlx90614 import MLX90614
bus = SMBus(1)
sensor = MLX90614(bus, address=0x5A)
print sensor.get_amb_temp()
print sensor.get_obj_temp()
bus.close()
,,,

7. By running this code, the temperature sensor starts working and it will print the
ambient and the object temperature.
8. Now after developing the program to annotate the text on the picture and running the
final program it will turn the Camera on and the body temperature will be visible now
the person’s image and the her/his body temperature will be shown.
9. Now by pressing Enter on the keyboard the image will be taken and will be stored in
the Output folder in local storage. 

## How it works:
• The prototype consists of a Raspberry Pi, MLX96014- Thermal Scanner, 7-inch LCD
display and a camera to click the image- RasPi Camera.
• As the hardware is set up, the device runs on Linux OS by running the program that has
been developed the camera will be enabled and the temperature sensor as well. The
sensor here takes a continuous data and it will be able to show the body temperature
annotated on the screen.
• As the camera is enabled the person will be able to see it’s face on the 7-inch LCD
display screen along with the temperature annotated at the bottom of the display.
• As the person’s face is kept near to the temperature sensor the body temperature will
be displayed. Now the picture has to be clicked and that picture will consist of the
person’s face and her/his body temperature.
• This picture will be sent to the server database.

## Usage: Over the Handheld Thermal Scanner/ Scanning Guns.

## Why should one use it: 
Right now, the only option to track the coronavirus patients
is to find out with whom they have been in contact where did they go but it becomes quite
difficult when tracking down that person. Once the picture is clicked and if that person has high
temperature, it will be easier for the government authority to track down that person as they
have its photograph and the person’s body temperature as well.
Hence one the people are easily tracked the overall process will become faster and the
government can come up with preventive measures quickly to tackle Covid-19 and will be able
to prevent it up to some extent. 

## Benefit of using it:
The thermal scanners available right now costs around 7k to 8k
Rupees but the over all cost of making this device(prototype) is around 3000/- and once it is
converted into mass production(making it as a full scale device) it can cost around 1500/-,
this will be very cheap and efficient for the government along with supporting the
#makeinIndia movement.

## Future scope: 
By making the device GPS enabled the location of the person can be
tracked along with its picture.

## Acknowledgements: 
I am grateful to our Principal Shri I. N. Patel sir, our HOD Dr.
Bhargav Goradiya and faculty members of EC department for helping me and motivating me
for making the project successful. 
