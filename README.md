# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-19 at 8 56 49 PM](https://github.com/user-attachments/assets/624ee900-ca11-4884-84ce-4f4a9490c7a2)
![WhatsApp Image 2025-11-19 at 8 56 50 PM](https://github.com/user-attachments/assets/b7f339f3-35f3-49b3-ad5d-f53e600ad6a4)
![WhatsApp Image 2025-11-19 at 8 56 50 PM (1)](https://github.com/user-attachments/assets/0fc427f5-850b-4487-ba08-e8d24311c676)



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[1];
den=[0.05 0.6 1 0];
sys=tf(num,den)
bode(sys)
grid on;
[gm pm wpc wgc]=margin(sys)
gmindb=20*log10(gm)
if(wpc>wgc)
    disp('stable')
elseif(wpc==wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:

<img width="1919" height="957" alt="Screenshot 2025-11-05 085237" src="https://github.com/user-attachments/assets/2589d836-8501-4260-b2ab-1bb92a123c79" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin =12 dB <br>
Phase Margin = 60 degree<br>
Gain crossover frequency =0.9070 rad/s. <br>
Phase crossover frequency =4.4721. <br>
The system is  stable.
