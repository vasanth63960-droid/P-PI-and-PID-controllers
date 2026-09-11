# Analysis of P, PI and PID Controllers using MATLAB
## Aim:
To analyse the effect of P, PI and PID controllers for the system having open loop transfer function, G(S)=1/(S^2+10S+20) using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
	A controller is a device introduced in the system to modify the error signal and to produce a control signal. 
	The way the controller produces the control signal is called the control action.

Consider the following unity feedback system,
 <img width="823" height="281" alt="image" src="https://github.com/user-attachments/assets/36e49512-cf47-4fec-b00c-f79dc0af1c5f" />

### Proportional (P) Controller:
The proportional controller produces an output, which is proportional to error signal.<br>
u(t)∝e(t) <br>
⇒u(t)=Kpe(t) <br>
Apply Laplace transform on both the sides - <br>
U(s)=KpE(s) <br>
U(s)/E(s)=Kp <br>
Therefore, the transfer function of the proportional controller is Kp.

### Proportional Integral (PI) Controller:
The proportional integral controller produces an output, which is the combination of outputs of the proportional and integral controllers. <br>
u(t)=Kp e(t)+Ki ∫e(t)dt <br>
Apply Laplace transform on both sides - <br>
U(s)=(Kp+Ki/s)E(s) <br>
U(s)/E(s)=Kp+Ki/s <br>
Therefore, the transfer function of proportional integral controller is Kp+Kis. <br>

### Proportional Integral Derivative (PID) Controller:
The proportional integral derivative controller produces an output, which is the combination of the outputs of proportional, integral and derivative controllers. <br>
u(t)=Kp e(t)+Ki ∫e(t)dt+ Kd (de(t)/dt) <br>
Apply Laplace transform on both sides - <br>
U(s)=(Kp+Ki/s+Kds)E(s) <br>
U(s)/E(s)=Kp+Ki/s+Kd s <br>
Therefore, the transfer function of the proportional integral derivative controller is Kp+Ki/s+Kd s

### Characteristics of Kp, Ki and Kd terms:

Increasing the proportional gain ( ) has the effect of proportionally increasing the control signal for the same level of error. The fact that the controller will "push" harder for a given level of error tends to cause the closed-loop system to react more quickly, but also to overshoot more. Another effect of increasing   is that it tends to reduce, but not eliminate, the steady-state error.
The addition of a derivative term to the controller ( ) adds the ability of the controller to "anticipate" error. With derivative control, the control signal can become large if the error begins sloping upward, even while the magnitude of the error is still relatively small. This anticipation tends to add damping to the system, thereby decreasing overshoot. The addition of a derivative term, however, has no effect on the steady-state error.
The addition of an integral term to the controller ( ) tends to help reduce steady-state error. If there is a persistent, steady error, the integrator builds and builds, thereby increasing the control signal and driving the error down. 
 


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the steady state error and analyse the controllers.
## Program: 
### Without Controller (Open loop System)
<img width="636" height="243" alt="image" src="https://github.com/user-attachments/assets/71411494-b69a-477c-8331-6463cd909d71" />



### With P-Controller
<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/d06cc1af-46c5-43e2-8e3d-2e1bfa2712b5" />


### With PI Controller
<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/13b76338-d7df-4afc-9839-ae7a45ac5c05" />


### With PID Controller
<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/02be7a54-5ddb-45ec-aa52-0d8261884c69" />


## Output: 
### Without Controller (Open loop System)
<img width="840" height="634" alt="image" src="https://github.com/user-attachments/assets/ed027119-773b-41d2-8950-beceabe99342" />



### With P-Controller
<img width="832" height="627" alt="image" src="https://github.com/user-attachments/assets/2ca8a1aa-cbf2-46fc-af42-3a7d01d6782c" />


### With PI Controller
<img width="843" height="640" alt="image" src="https://github.com/user-attachments/assets/3dffb587-5171-4c90-ab3d-4e2f04821c50" />


### With PID Controller
<img width="839" height="631" alt="image" src="https://github.com/user-attachments/assets/a5a45387-1a30-4de9-89f2-02bf801579e1" />



## Result:
Thus the P, PI and PID controllers for the given system was analysed and the following conclusions were arrived using MATLAB. <br>
### With-out controller 
Delay time =         <0.5s>
Rise time =             <1s>
Peak time =           <2s>
Settling time =            <2s>
Steady State Error =        <0.95>
### With P Controller 
Delay time =         <0.1s>
Rise time =             <0.2s>
Peak time =           <0.3s>
Settling time =            <1s>
Steady State Error =        <0.12>
### With PI Controller 
Delay time =         <0.1s>
Rise time =             <0.175s>
Peak time =           <0.25s>
Settling time =            <3s>
Steady State Error =        <0>
### With PID Controller 
Delay time =         <0.01s>
Rise time =             <0.05s>
Peak time =           <1s>
Settling time =            <2.6s>
Steady State Error =        <0>




