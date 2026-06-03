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

```spice
Title:ID-VS-VGS for NMos in saturation region

*level-1 Model
.MODEL nmos1 NMOS (LEVEL=1 PHI=0.846 VTO-0.514 KP=122U GAMMA=0.55 LAMBDA=0.0)

*Set the device temperature
.TEMP 27

*netlist
```
![ID vs VGS](ID%20vs%20VGS2.png)
![ID vs VGS](ID%20vs%20VGS3.png)

# Lab 3: NGSPICE

##

