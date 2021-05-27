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

%First Joint can label position 
uicontrol('style',"text","String","First Joint Position","Position", ...
    [50 100 100 30]);
%Create box for first joint position
uicontrol('Style','edit', "Position", [50 50 100 30]); 

%Second Joint can label position
uicontrol('style',"text","String","Second Joint Position","Position", ...
    [200 100 100 30]);
%Create box for second joint position
uicontrol('Style','edit', "Position", [200 50 100 30]); 

%Third Joint label position
uicontrol('style',"text","String","Third Joint Position","Position", ...
    [350 100 100 30]);
%Create box for third joint position
uicontrol('Style','edit', "Position", [350 50 100 30]); 

%Fourth Joint label position
uicontrol('style',"text","String","Fourth Joint Position","Position", ...
    [500 100 100 30]);
%Create box for fourth joint position
uicontrol('Style','edit', "Position", [500 50 100 30]); 

%Create x value label 
uicontrol('style','text', "String", "X Value","BackgroundColor",'red',...
    'Position',[125 250 75 10]);
%Create box for x value
uicontrol('Style','edit', "Position", [110 200 100 30]);

%Create y value label 
uicontrol('style','text', "String", "Y Value","BackgroundColor",'blue',...
    'Position',[275 250 75 10]);
%Create box for y value
uicontrol('Style','edit', "Position", [265 200 100 30]);

%Create z value label 
uicontrol('style','text', "String", "Z Value","BackgroundColor",'green',...
    'Position',[425 250 75 10]);
%Create box for z value
uicontrol('Style','edit', "Position", [415 200 100 30]);
