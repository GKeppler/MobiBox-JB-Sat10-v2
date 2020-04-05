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

## DSP
[ADAU1701](https://www.analog.com/media/en/technical-documentation/data-sheets/ADAU1701.pdf) DSP Chip  

### programming:  
https://www.360customs.de/2015/01/sigmadsp-programmieren-sigma-studio-adau17011401a-eeprom-standalone-self-boot/  
https://ez.analog.com/dsp/sigmadsp/f/q-a/65081/adau1701-not-programming
https://suredsp.ratz-it.de/index.php?title=Treiber_installieren

### audio-filters/effects
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
- light 10" (2.2 kg) for ferrit-magnet chassis
- 4 Ohm

things to think about:  
- 10FE200 Q_ts 0.54 not optimal for Bassreflex, but EPB of 105  
- needs bassboost for Fullrange use -> DSP

alternative bassdrivers: [loudspeakerdatabase](http://www.loudspeakerdatabase.com/search/type=Subwoofer,Woofer,Mid_Bass,Mid-range,Full-range/8.0_size_in_12.0/1_z_4/100_pw_500/94.0_spl_118.0/9_fs_70/0.13_qts_0.70/sort=-spl)

### Sica z009442 + Q07032B

- 1" plastic tweeter horn
- 8 Ohm

## Box
idea: https://youtu.be/EEh01PX-q9I?t=2532 but flexibel 2k-PU is used -> cheaper than Decidamp

Sandwich poplar plywood-> 6mm plywood, ~1mm PU, 6mm plywood  
- stiff
- sounddamping
- light (ca. 3kg wood for the hole boy)

## Boxsim Simulation
![SPL](Simulation/SPL.jpg)
![Richtcharakteristik](Simulation/Richtcharakteristik.jpg)


