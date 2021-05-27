# Required Joints-GUI

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
uicontrol("Style","text","String","Inverse Kinematics GUI", "Position", ...
    [250 400 200 30]);

%First waste can label position 
uicontrol('style',"text","String","First Waste Can Position","Position", ...
    [50 100 100 30]);
%Create box for first waste can position
uicontrol('Style','edit', "Position", [50 50 100 30]); 

%Second waste can label position
uicontrol('style',"text","String","First Waste Can Position","Position", ...
    [200 100 100 30]);
%Create box for second waste can position
uicontrol('Style','edit', "Position", [200 50 100 30]); 

%Third waste can label position
uicontrol('style',"text","String","First Waste Can Position","Position", ...
    [350 100 100 30]);
%Create box for third waste can position
uicontrol('Style','edit', "Position", [350 50 100 30]); 

%Fourth waste can label position
uicontrol('style',"text","String","First Waste Can Position","Position", ...
    [500 100 100 30]);
%Create box for fourth waste can position
uicontrol('Style','edit', "Position", [500 50 100 30]); 
