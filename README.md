# Two_stage_opamp_with_miller_compensation
..

This project presents the design and optimization of a two-stage CMOS operational amplifier targeted for low-power, high-speed analog applications. The amplifier was designed to operate with a 5 pF capacitive load while meeting stringent performance constraints on power, stability, and bandwidth.


The project flow goes as follows:
1. Declaring design specifications.
2. calculating the DC parameter using DC analysis of nmos and pmos (μpCox and μnCox).
3. calculating the min and max threshold value of m1 and m3 mos
4. designing full circuit and make proper wire connection
5. check all mosfet working region through DC analysis
6. ploting bode plot through ac analysis
7. checking all other parameter ( CMRR , slew rate , Noise , PSRR , Power dissipation )


🔧 Design Constraints

Load Capacitance (CL): 5 pF
Power Consumption: < 0.5 mW
Unity-Gain Bandwidth (UGB): > 10 MHz
Slew Rate: ≥ 15 V/µs
DC Gain: > 60 dB
Phase Margin (PM): > 75°

📊 Achieved Performance

DC Gain: > 70 dB
Unity-Gain Bandwidth: ~22 MHz
Phase Margin: > 80° (≈86° worst-case)
Slew Rate: ~13 V/µs
Power Consumption: < 0.3 mW
Strong low-frequency PSRR (~72 dB) and CMRR (> 70 dB)

 ## Calculating the DC parameter using Dc analysis of nmos and pmos (μpCox and μnCox)

upcox = 60u , 
uncox = 325u

![betaeffctive](https://github.com/user-attachments/assets/173a8a26-fb37-4621-9ef3-be2dd1d0dc9e)


## Calculating the min and max threshold value of m1 and m3 mos

Vtpmin = Vtpmax = 500mV ,
Vtnmin = 450mV, Vtnmax = 550mV

## Designing full circuit and make proper wire connection

![nmos2stageSchematic](https://github.com/user-attachments/assets/14fdaabc-4ac1-4e3b-9520-b95aca139718)


## Ac analysis ( Bode plot) 
**DCGain=52dB , GBW = 39.21MHz and Phase Margin = 61.93 , Bandwidth=164kHz**

![nmos2stageacjpg](https://github.com/user-attachments/assets/3b06c168-f859-49b6-acd4-2d3f92ba032a)


## Calculation of Slew Rate.

![nmos2stageSR](https://github.com/user-attachments/assets/0c50c973-4d14-4114-a126-d7160c56de1a)


from the wave output we get 𝗦𝗥 = 𝟯𝟯.𝟵 𝘃/𝘂𝘀𝗲𝗰 

## CMRR Plot

![pmos2stage_cmrr](https://github.com/user-attachments/assets/958e63b6-099f-41cb-994f-03875ab1c4fc)


## PSRR Plot
![pmos2stage_psrr2](https://github.com/user-attachments/assets/b7f85af2-b525-433d-aeff-f90810a1ac32)






