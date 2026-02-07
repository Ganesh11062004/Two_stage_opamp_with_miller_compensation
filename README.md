# Two_stage_opamp_with_miller_compensation


This project presents the design and optimization of a two-stage CMOS operational amplifier targeted for low-power, high-speed analog applications. The amplifier was designed to operate with a 5 pF capacitive load while meeting stringent performance constraints on power, stability, and bandwidth.
**I used the UMC180nm technology for this project**


The project flow goes as follows:
1. Declaring design specifications.
2. calculating the DC parameter using DC analysis of nmos and pmos (μpCox and μnCox).
3. calculating the min and max threshold value of m1 and m3 mos
4. designing full circuit and make proper wire connection
5. check all mosfet working region through DC analysis
6. ploting bode plot through ac analysis
7. checking all other parameter ( CMRR , slew rate , Noise , PSRR , Power dissipation )


🔧 Design Constraints

- Load Capacitance (CL): 5 pF
- Power Consumption: < 0.5 mW
- Unity-Gain Bandwidth (UGB): > 10 MHz
- Slew Rate: ≥ 15 V/µs
- DC Gain: > 60 dB
- Phase Margin (PM): > 75°

📊 Achieved Performance

- DC Gain: > 70 dB
- Unity-Gain Bandwidth: ~22 MHz
- Phase Margin: > 80° (≈86° worst-case)
- Slew Rate: ~13 V/µs
- Power Consumption: < 0.3 mW
- Strong low-frequency PSRR = ~72 dB and CMRR > 75 dB

**Design Methodology**

Conventional Miller compensation resulted in a phase margin of approximately 57° due to a right-half-plane zero. A nulling resistor was added in series with the Miller capacitor to shift the zero to the left-half plane, improving the phase margin to >80° without sacrificing bandwidth or power efficiency.

 ## Calculating the DC parameter using Dc analysis of nmos and pmos (μpCox and μnCox)

upcox = 60u , 
uncox = 325u

![](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/test_ckts/Vth.png)


## Calculating the min and max threshold value of m1 and m3 mos
![](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/test_ckts/test.png)
**Vtpmin = Vtpmax = 500mV**

**Vtnmin = 450mV, Vtnmax = 550mV**

## Designing full circuit and make proper wire connection

![](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/Schematic/op_amp_with_Cc.png)


## Ac analysis ( Bode plot) 
**DCGain=73.89dB , GBW = 21.6MHz and Phase Margin > 85° , Bandwidth=164kHz**

![](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/simulation_outputs/gain_phaze.png)

Adl Window
![](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/simulation_outputs/gain_phaze_adl.png)

## Gain and Phaze plot without nulling resistor
![](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/simulation_outputs/gain_phaze_without_Rn.png)
## CMRR Plot

![pmos2stage_cmrr](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/simulation_outputs/cmrr.png)


## PSRR Plot
![pmos2stage_psrr2](https://github.com/Ganesh11062004/Two_stage_opamp_with_miller_compensation/blob/d6ce5ec575ba977f699ca368110c29a177deb796/simulation_outputs/psrr.png)






