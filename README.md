%Required Joint Angles GUI

%Clear workspace area and command 
clc;
clear;
%Closes any existing graphs 
close all; 
format compact

%Create a large figure for GUI and position
f=figure('position', [0 0 700 500], 'name', 'GUI', 'NumberTitle', 'off');

%Create subplot to hold plot 
h = subplot('Position', [-3500 3500 0 3000]);

%Title
uicontrol("Style","text","String","Required Joints GUI", "Position", ...
    [250 400 200 30]);

%First Waste Can position can label position 
uicontrol('style',"text","String", "First Waste Can Position","Position", ...
    [50 100 100 30]);
%Create box for First Waste Can position
uicontrol('Style','edit', "Position", [50 50 100 30]); 

%Second Waste Can label position
uicontrol('style',"text","String","Second Waste Can Position","Position", ...
    [200 100 100 30]);
%Create box for Second Waste Can position
uicontrol('Style','edit', "Position", [200 50 100 30]); 

%Third Waste Can label position
uicontrol('style',"text","String","Third Waste Can Position","Position", ...
    [350 100 100 30]);
%Create box for Third Waste Can position
uicontrol('Style','edit', "Position", [350 50 100 30]); 

%Fourth Waste Can label position
uicontrol('style',"text","String","Fourth Waste Can Position","Position", ...
    [500 100 100 30]);
%Create box for Fourth Waste Can position
uicontrol('Style','edit', "Position", [500 50 100 30]); 

%Create x value label 
uicontrol('style','text', "String", "X Value","BackgroundColor",'red',...
    'Position',[500 400 75 10]);
%Create box for x value
uicontrol('Style','edit', "Position", [500 360 100 30]);

%Create y value label 
uicontrol('style','text', "String", "Y Value","BackgroundColor",'blue',...
    'Position',[500 320 75 10]);
%Create box for y value
uicontrol('Style','edit', "Position", [500 280 100 30]);

%Create z value label 
uicontrol('style','text', "String", "Z Value","BackgroundColor",'green',...
    'Position',[500 250 75 10]);
%Create box for z value
uicontrol('Style','edit', "Position", [500 210 100 30]);

%Declaring Variables for Joint 1
theta1 = 0
alpha1 = 0
d1 = 1300
a1 = 35
 
%Declaring Variables for Joint 2
theta2 = 90
alpha2 = 180
d2 = 1400
a2 = 45

%Declaring Variables for Joint 3
theta3 = 90
alpha3 = -90
d3 = 0
a3 = 45

%Declaring Variables for Joint 4
theta4 = 0 
alpha4 = 0
d4 = 0
a4 = 45


%Adding DH table for the joints
base = [1 0 0 0; 0 1 0 0; 0 0 0 1]

%Joint 1 Variables
J1rotz = [cosd(theta1) -sind(theta1) 0 0; sind(theta1)...
    cosd(theta1) 0 0; 0 0 1 0; 0 0 0 1];
J1transz = [1 0 0 0; 0 1 0 0; 0 0 1 d1; 0 0 0 1]
J1transx = [1 0 0 a1; 0 1 0 0; 0 0 1 0; 0 0 0 1]
J1rotx = [1 0 0 0; 0 cosd(alpha1) -sind(alpha1) 0; ...
    0 sind(alpha1) cosd(alpha1) 0; 0 0 0 1]

Joint1 = J1rotz*J1transz*J1rotx*J1transx

%Joint 2 variables
J2rotz = [cosd(theta2) -sind(theta2) 0 0; sind(theta2)...
    cosd(theta2) 0 0; 0 0 1 0; 0 0 0 1];
J2transz = [1 0 0 0; 0 1 0 0; 0 0 1 d2; 0 0 0 1]
J2transx = [1 0 0 a2; 0 1 0 0; 0 0 1 0; 0 0 0 1]
J2rotx = [1 0 0 0; 0 cosd(alpha2) -sind(alpha2) 0; ...
    0 sind(alpha2) cosd(alpha2) 0; 0 0 0 1]

Joint2 = J2rotz*J2transz*J2rotx*J2transx

%Joint 3 variables
J3rotz = [cosd(theta3) -sind(theta3) 0 0; sind(theta3)...
    cosd(theta3) 0 0; 0 0 1 0; 0 0 0 1];
J3transz = [1 0 0 0; 0 1 0 0; 0 0 1 d3; 0 0 0 1]
J3transx = [1 0 0 a3; 0 1 0 0; 0 0 1 0; 0 0 0 1]
J3rotx = [1 0 0 0; 0 cosd(alpha3) -sind(alpha3) 0; ...
    0 sind(alpha3) cosd(alpha3) 0; 0 0 0 1]

Joint3 = J3rotz*J3transz*J3rotx*J3transx

%Joint 4 Variables
J4rotz = [cosd(theta4) -sind(theta4) 0 0; sind(theta4)... 
    cosd(theta4) 0 0;0 0 1 0; 0 0 0 1];
J4transz = [1 0 0 0; 0 1 0 0; 0 0 1 d4; 0 0 0 1]
J4transx = [1 0 0 a4; 0 1 0 0; 0 0 1 0; 0 0 0 1]
J4rotx = [1 0 0 0; 0 cosd(alpha4) -sind(alpha4) 0; ...
    0 sind(alpha4) cosd(alpha4) 0; 0 0 0 1]

Joint4 = J4rotz*J4transz*J4rotx*J4transx
