# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: Initiate the MobileRobot.
<br/>

Step2: Connect your PC with the MobileRobot through Wi-Fi.

<br/>

Step3: Open batter_level.py file and check the battery.

<br/>

Step4: Open the other Python files and Program the movements of the robot using python.

<br/>

Step5: Execute the python program and record the movements.

<br/>

## Program
```
#Developed by:JAYASRI DODDA
#Register number: 212222240028

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera
          
    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
    ''' 
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5] 
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second)  [0.5,2]

    '''
    ep_chassis.move(x=2, y=0, z=0, xy_speed=0.95).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=204,g=255,b=255,effect="on") 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=204,g=204,b=255,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on")
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on") 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on")
    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on") 
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on")
    


  
 
 
    
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)
### Initial position:

![intittttt](https://github.com/jayasridodda/mobilerobot-openloopcontrol/assets/123259278/c12cd20f-1880-4627-82bc-95d35ae39da7)
### Final Position:
![Screenshot (75)](https://github.com/jayasridodda/mobilerobot-openloopcontrol/assets/123259278/57d3492b-31ad-4c93-b650-b13e27748d77)




<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:
https://youtu.be/nZMAdS07Pls

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
