# MobiBox-JB-Sat10-v2 aka Soundklotz, Soundmops, Soundtrotz, Soundrocks

general Ideas: http://www.hifi-forum.de/viewthread-331-139.html#top

## Amplifier 

2x TPA3116 
https://de.aliexpress.com/item/4000099713796.html  
-cheap
-bluetooth integrated

## Battery

5s2p 18650 Lipo's with BMS ca. 7Ah
- high output power
- light

## DSP [ADAU1701](https://www.analog.com/media/en/technical-documentation/data-sheets/ADAU1701.pdf)
- phone app called "Advanced Spectrum Analyzer" for tuning

write:  ./eeprog -f -16  -i epr.hex  -w 0x00 -t 5 /dev/i2c-1 0x50
read:   ./eeprog -xf /dev/i2c-1 0x50 -16 -r 0x00:0x100
read2:   i2cdump -y 1 0x50 i

Die normalen, analogen Ausgänge sind intern nur als DAC0, DAC1, etc. benannt. Auf dem Sure DSP sind diese wie folgt beschriftet: DAC0-OutR1, DAC1-OutL1, DAC2-OutR2, DAC3-OutL2. 

OutR2 -> DAC2
OutR1 -> DAC0

Pinout sure dsp: https://suredsp.ratz-it.de/images/e/ee/Pinbelegung_SureDSP_neu.png
programmieren 2:
https://www.richud.com/wiki/Rasberry_Pi_I2C_EEPROM_Program
https://github.com/tat/eeprog/blob/master/eeprog.c


ADC0 & ADC1 18 kOhm & 47 μF capacitor audio input: 
The external resistor connected to ADC_RES sets the full-scale
current input of the ADCs. The full range of the ADC inputs is
100 µA rms with an external 18 kΩ resistor on ADC_RES (20 kΩ
total, because it is in series with the internal 2 kΩ). The only
reason to change the ADC_RES resistor is if a sampling rate
other than 48 kHz is used.
For these three resistors, a 1% tolerance is
recommended.

. The 47 μF capacitors are
used to ac-couple the signals so that the inputs are biased at 1.5 V

DAC0 - ADC3 560 Ohm & 47 μF ac-couple-capacitor & 5,6nF low pass(50 kHz -3dB) audio output:

### programming:  

https://www.360customs.de/2015/01/sigmadsp-programmieren-sigma-studio-adau17011401a-eeprom-standalone-self-boot/  
https://ez.analog.com/dsp/sigmadsp/f/q-a/65081/adau1701-not-programming
https://suredsp.ratz-it.de/index.php?title=Treiber_installieren

programm using raspberry pi and [this](https://www.richud.com/wiki/Rasberry_Pi_I2C_EEPROM_Program) guide
1.check: sudo i2cdetect -y 1     ->e.g 0x50
2.read: i2cdump -y 0 0x50 i 
3.write: ./eeprog -f -8 -i hex.file -w 0x00 -t 5 /dev/i2c-1 0x50

### audio-filters/effects:

[Psychoakustik & Psychoakustik-Effekte](https://curdt.home.hdm-stuttgart.de/PDF/Psychoakustik_und_Psychoakustik_Effekte.pdf)
https://ez.analog.com/dsp/sigmadsp/f/q-a/65338/dynamic-bass-boost-basics
https://wiki.analog.com/resources/tools-software/sigmastudio/toolbox/adialgorithms/automaticspeakereq
https://eclipseaudio.com/fir-filter-guide/

## PA-box reference [JB-Sat10-v2](https://www.lautsprecherforum.eu/viewtopic.php?t=4907)  
 
<img src="https://www.lautsprecherforum.eu/images/files/x_id_high_3_1967.jpg" alt="drawing" width="200"/> 

- Faital 10FE200 / Sica z009442 +Q07032B)  
- 96dB 1W/1m  
- 118dB (121dB Max / 124dB Peak) 
- 165W rms  
- 80Hz - 20,3kHz  
- 75x50°

changes:  

- 4 Ohm Faital 10FE200 to get more power out of the TPA3116
- BR-Box for higher bass efficency

### Faital 10FE200 
  
- cheap PA-chassis
- high soundpreassurelevel & efficency
- light 10" (2.2 kg) for a ferrit-magnet chassis
- 4 Ohm

things to think about:  
- Q_ts 0.54 not optimal for Bassreflex, but EPB of 105  
- needs bassboost for Fullrange use -> DSP

alternative bassdrivers: [loudspeakerdatabase](http://www.loudspeakerdatabase.com/search/type=Subwoofer,Woofer,Mid_Bass,Mid-range,Full-range/8.0_size_in_12.0/1_z_4/100_pw_500/94.0_spl_118.0/9_fs_70/0.13_qts_0.70/sort=-spl)

### Sica z009442 + Q07032B

- 1" PA tweeter horn
- 8 Ohm

## Box

### dimensions
- 32*30*42cm outside messure  
- sandwich poplar plywood structure-> 6mm plywood, ~0.2mm PU, 6mm plywood  
	- idea: https://youtu.be/EEh01PX-q9I?t=2532 but flexibel 2k-PU is used -> cheaper than Decidamp
	- stiff
	- sounddamping
	- light (ca. 3kg wood for the hole boy)

### Bassreflex

The chassis is relieved of stress near the tuning frequency, but below that the housing no longer represents resistance and the diaphragm deflection is significantly higher
->variable bassboost - strong bass for low volume and weak bass for higher volume

## Boxsim Simulation

![SPL](Simulation/SPL.jpg)
![Richtcharakteristik](Simulation/Richtcharakteristik.jpg)


