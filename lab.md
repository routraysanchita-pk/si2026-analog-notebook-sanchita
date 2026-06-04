# Lab Notebook

Maintain Lab notebook here.

# Lab 1: Linux, Vim and Git

## 1.BASIC LINUX COMMAND
Commands used are:
- 'echo'
- 'pwd'
- 'cd'
- 'ls'
  and others
   
![Linux Command](LINUX%20COMMAND.png)

## 2. FILE AND DIRECTORY HANDLING COMMANDS
Commands used are:
- 'mkdir'
- 'touch'
- 'rm'
- 'rmdir'
  and others
  
![Linux Command](LINUX%20COMMAND1.png)

# Lab 2: NGSPICE

## 1.VOLTAGE DIVIDER

Voltage Divider Netlist/Circuit Was Simulated Successfully 

```spice
* This is netlist/circuit of a simple voltage divider
  
R1 vin vout 1K
R2 vout 0 1K

*Pulse StimulusVpulse vin 0 PULSE(0 5 0.5u 10n 10n 0.5u 1u)

*Transient Analysis
.TRAN 0.1u 1.5u

.control
RUN
PLOT V(vout)
.endc

.end
```

Output Voltage was observed from the simulation

![Voltage Divider Netlist](VOLTAGE%20DIVIDER1.png)

## 2.ID vs VGS

The variation of drain current with gate-sourse voltage was studied.

## ID vs VGS

The variation of drain current with gate-source voltage was analyzed.

```spice
Title: Id-vs-Vgs for NMOS in Saturation region

* Level-1 Model
.MODEL nmos1 NMOS (LEVEL=1 PHI=0.846 VTO=0.514 KP=122U GAMMA=0.55 LAMBDA=0.0)

* Set the device temperature
.TEMP 27

* Netlist
M2 D2 D2 0 B nmos1 W=5u L=1u
Vds D 0 DC 5
Vid2 D D2 DC 0
Vsb 0 B DC 0

* DC Sweep Analysis
.DC Vds 0 5 0.001 Vsb 0 1 0.5

.CONTROL
RUN
PLOT Vid2#branch vs V(D)
PLOT (2*Vid2#branch)^0.5 vs V(D)
.ENDC

.END
```

![ID vs VGS](ID%20vs%20VGS2.png)
![ID vs VGS](ID%20vs%20VGS3.png)

# Lab 3: NGSPICE

##

