%ELEC 4700 MNA Building
%Narrthanan Seevananthan

%Equations in use:
%V = IR
%I = C(dV/dt)
%V = L(dI/dt)

%Component Values
R1 = 1;
C = 0.25;
R2 = 2;
L = 0.2;
R3 = 10;
alpha = 100;
R4 = 0.1;
RO = 1000;

%Differential Equations from left to right:
%N1:
% Ix1 - (VN1-VN2)/R1 - C*(d(VN1-VN2)/dt) = 0;
% VN1 = Vin;
% %Ix1 = current passing through Voltage source Vin
% 
% %N2:
% (VN1-VN2)/R1 + C*(d(VN1-VN2)/dt) - VN2/R2 - IL = 0;
% (VN2-VN3) = L*(dIL/dt);
% 
% %N3:
% IL - VN3/R3 = 0;
% I3 = VN3/R3;
% 
% %N4:
% Ix2 - (VN4-VN5)/R4 = 0;
% VN4 = alpha*I3;
% %Ix2 = current passing through current dependent voltage source @ N4
% 
% %N5:
% (VN4-VN5)/R4 - VN5/RO = 0;
% 
% 
% 
% %Differential Equations from left to right (Frequency Domain):
% %N1:
% Ix1 - (VN1-VN2)/R1 - C*(j*w*VN1(w) - j*w*VN2(w)) = 0;
% VN1 = Vin;
% %Ix1 = current passing through Voltage source Vin
% 
% %N2:
% (VN1-VN2)/R1 + C*(j*w*VN1(w)-j*w*VN2(w)) - VN2/R2 - IL = 0;
% (VN2-VN3) = L*(j*w*IL(w));
% 
% %N3:
% IL - VN3/R3 = 0;
% I3 = VN3/R3;
% 
% %N4:
% Ix2 - (VN4-VN5)/R4 = 0;
% VN4 = alpha*I3;
% %Ix2 = current passing through current dependent voltage source @ N4
% 
% %N5:
% (VN4-VN5)/R4 - VN5/RO = 0;  %VN5 = VO

G = zeros(9,9);
C = zeros(9,9);

G(1,1) = G(1,1) - (1/R1);
G(2,1) = G(2,1) + (1);
G(3,1) = G(3,1) + (1/R1);

G(1,2) = G(1,2) + (1/R1);
G(3,2) = G(3,2) - (1/R1) - (1/R2);
G(4,2) = G(4,2) + (1);

G(4,3) = G(4,3) + (-1);
G(5,3) = G(5,3) + (-1/R3);
G(6,3) = G(6,3) + (-1/R3);

G(7,4) = G(7,4) + (-1/R4);
G(8,4) = G(7,4) + (1);
G(9,4) = G(7,4) + (1/R4);

%VO = VN5 is the output, plot this while varying Vin
%AC sweep vary (w) 
