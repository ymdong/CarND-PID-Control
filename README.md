# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

In this project, I implement the PID control for an autonomous car dring in the track. In PID algorithm, we need to tune three gains Kp, Ki and Kd, which correspond to the proportional, integral and derivative control. For the propotional term, if we increase Kp, the steady state error can be reduced but the system responsse tends to osillate. For the integral term, if we increase Ki, the steady state error can be reduced but the system response speed become slow. For the derivative term, if we increase Kd, the system reponse speed can be faster because the future informaiton is utilized for derivative term. 

The parameters tuning is done manually:

First, I set Kp=0.2, Ki=0, Kd=0, then I observe that the car's trajectory is osillating, which indicates I should decrease the Kp. 

Next, I set Kp=0.1, Ki=0, Kd=2, I observe that the car can drive through the track successfully, but in the sharp turn, the steering action is a bit slow, which indicates I should increase Kd. It also doesn't stay in the center of lane all the time, which indicates I should increase Ki.

Then, I set Kp=0.1, Ki=0.002, Kd=4, I find that the car can drive through the track successfully and can handle the sharp turn well. 

