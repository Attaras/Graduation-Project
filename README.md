# Graduation-Project
An intelligent robotic leg actuated via muscle signals using a neural network.

# EMG Controlled Prosthetic Robot Leg

In this repository i put all the code i'll explain the workings of the project and the all the implementations involved.

## Components Used:
- Arduino Uno Board
- EMG V3 Muscle Sensors
- High Torque Servo Motor
- Angle reading Gyroscopes

## Muscle Signal/Angle  Reading:

Both the muscle signal and the angle readings were taken concurrently.

![alt text](https://raw.githubusercontent.com/Attaras/Graduation-Project/master/Reading%20Circuit.png)

- The Code
```arduino
   Graduation-Project/Data_Acquisition_Code.ino
```
## Analysis with Excel:
The siganls were taken to excel where they were filtered.
The gyroscope gave back very precise readings, with 2 decimal points which were ceiled/floored to make mapping easier for the neural net.

- before smoothing:

![alt text](https://raw.githubusercontent.com/Attaras/Graduation-Project/master/beforefiltering.png)

- after smoothing:

![alt text](https://raw.githubusercontent.com/Attaras/Graduation-Project/master/afterfiltering.png)

## Neural Network:
The neural network was trained to output angle commands to the motors in response to muscle signals.
The library that was used was Keras.

![alt text](https://raw.githubusercontent.com/Attaras/Graduation-Project/master/nn.png)

## Actuation Circuit:
The neural network model was implemented into the arduino and was used to calculate the required angle for the muscle signals in real time.

![alt text](https://raw.githubusercontent.com/Attaras/Graduation-Project/master/Actuation.png)

- The Code:
```arduino
   Graduation-Project/Neural_Network_Arduino_Implementation   
```
//youtube link

## Contributing
This prosthetic leg was created as my graduation project with my project pair Tamim.
