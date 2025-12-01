# Stability-Analysis-using-Bode-Plot

## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 

## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-27 at 18 27 03_911cb09c](https://github.com/user-attachments/assets/977875e4-a319-4ba5-9e79-d0d03ef44dfb)
![WhatsApp Image 2025-11-27 at 18 27 02_2b8b6437](https://github.com/user-attachments/assets/f8fd972c-829a-44ae-a1ef-1c69edb92b4b)
![WhatsApp Image 2025-11-27 at 18 27 02_d6d22b0f](https://github.com/user-attachments/assets/214724ec-d3c2-4e40-bfce-7b3417d208d6)

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program:

```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:

<img width="707" height="630" alt="image" src="https://github.com/user-attachments/assets/c43c55ab-6b64-4424-827f-8ff179b29b97" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 <br>
Phase Margin = 60 <br>
Gain crossover frequency = 0.907 <br>
Phase crossover frequency = 4.4721 <br>
The system is stable.
