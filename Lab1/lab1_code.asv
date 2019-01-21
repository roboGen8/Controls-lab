%%Question 1
clear;
clc;
close all;

A = [-0.02 0.1 0 -32.2; -0.04 -0.8 180 0; 0 -0.003 -1.0 0; 0 0 1 0];
B = [0; -8; -4; 0];
C = [0 0 0 1];
D = 0;

[V, S] = eig(A);
[num, den] = ss2tf(A, B, C, D);
G1 = tf(num, den);
zpk(G1);
G2 = tf2ss(num, den);
bode(G1);
C3 = [0 0 1 0; 0 0 0 1];
D3 = [0; 0];
G3 = ss(A, B, C3, D3);
step(0.02*G3);

% Answers:
% i) eigenvalues: 
% -0.9005 + 0.7293i, 
% -0.9005 - 0.7293i, 
% -0.0095 + 0.0528i, 
% -0.0095 - 0.0528i
%    corresponding eigenvalues: 
% v1 = 0.0314 - 0.0618i   v2 = 0.0314 + 0.0618i
%      0.9976 + 0.0000i        0.9976 + 0.0000i
%      -0.0005 + 0.0040i       -0.0005 - 0.0040i
%      0.0026 - 0.0024i        0.0026 + 0.0024i
% v3 = 0.9995 + 0.0000i   v4 = 0.9995 + 0.0000i
%      -0.0300 + 0.0005i       -0.0300 - 0.0005i
%      0.0001 - 0.0000i        0.0001 + 0.0000i
%      -0.0004 - 0.0016i       -0.0004 + 0.0016i
% 
% ii)             -4 s^2 - 3.256 s - 0.07952
%   -----------------------------------------------
%   s^4 + 1.82 s^3 + 1.38 s^2 + 0.0308 s + 0.003864
% 
% iii) The poles are equal to the eigenvalues
%   
% iv) G2 =
% 
%    -1.8200   -1.3800   -0.0308   -0.0039
%     1.0000         0         0         0
%          0    1.0000         0         0
%          0         0    1.0000         0
% This state space has only 0's and 1's in 2nd to 4th row
% Therefore the state space model looks different from the original one
%
% v) Bode plot shown in the next pages
%
% vi) Plot also shown in the next pages

%%Question 2
clear;
clc;
close all;

G = tf([2], [1 4 3 0]);
C = tf([1 0.5], [1 1]);
% rltool(G, C);
%%Question 3
clear;
clc;
close all;

Kp = 1;
Kd = 1;
G = tf([1], [1 0 0]);
C = tf([Kd Kp], [1]);
rltool(G, C);

%TF = 
%            1
%   --------------------
%   s^2 + 1.9 s + 0.5678
%poles: -1.5288, -0.3714
%Phase Margin: 81.2 degrees
%
%%Question 4
% clear;
% clc;
% close all;
% 
%
%%Question 5
%%Question 6
%%Question 7


