# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

In this project, I implement the PID control for an autonomous car dring in the track. 

In PID control, we need to tune three gains Kp, Ki and Kd, which correspond to the proportional, integral and derivative control. 
The proportional control produces an output value that is proportional to the current error value, which can correct the output deviation from the reference signal. But if we keep increasing Kp, the system can become unstable. The integral control accelerates the movement of the process towards setpoint and eliminates the residual steady state error that occurs with a pure proportional control, but it can cause overshoot. Derivative control predicts system behavior and thus improves settling time and stability of the system.

The parameters tuning is done manually:

First, I set Kp=0.2, Ki=0, Kd=0, then I observe that the car's trajectory is osillating, which indicates I should decrease the Kp. 

Next, I set Kp=0.1, Ki=0, Kd=2, I observe that the car can drive through the track successfully, but in the sharp turn, the steering action is a bit slow, which indicates I should increase Kd. It also doesn't stay in the center of lane all the time, which indicates I should increase Ki.

Then, I set Kp=0.1, Ki=0.002, Kd=4, I find that the car can drive through the track successfully and can handle the sharp turn well. 

