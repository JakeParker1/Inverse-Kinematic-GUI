# Inverse-Kinematic-GUI

%Inverse Kinematics GUI

%Clear workspace area and command 
clc;
clear;
%Closes any existing graphs 
close all; 
format compact

%Make a large figure 
figure('Position',[0 0 700 500], 'name', 'SimpleGUI', 'NumberTitle', 'off');

%Make subplot to hold plot 
h = subplot('Position', [-3500 3500 0 3000]);

%Title
uicontrol("Style","text","String","Inverse Kinematics GUI", "Position", ...
    [250 400 200 30]);

%Declare variables
%Length of first limb
L1 = 1300
%Length of second limb
L2 = 1400

%All possible theta1 values
theta1 = 0:0.1:pi/2;
%All possible theta2 values
theta2 = 0:0.1:pi;

%Create a grid showing theta1 and theta2 values
[Theta1, Theta2] = meshgrid (theta1,theta2);

%Generate x coordinates
x = L1 * cos(THETA1) + L2 * cos(THETA1 + THETA2);
%Generate y coordinates
y = L1 * sin(THETA1) + L2 * sin(THETA1 + THETA2);

%Create x-y-theta1 dataset
data1 = [x(:) y(:) THETA1(:)];
%Create x-y-theta2 dataset
data2 = [x(:) y(:) THETA2(:)];
