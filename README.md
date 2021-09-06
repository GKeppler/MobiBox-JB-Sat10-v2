# Soundklotz
Cheap bettery powered PA equipment. One Sattelite([JB-Sat10-v2](https://www.lautsprecherforum.eu/viewtopic.php?t=4907)) speaker and one Sub(PS-Bass V2) using 40V Li-Ion batteries from Elektric-Drills.

Can be used as portable Bluetooth Box with Sattelite standalone, or with the additional sub for some serious bass.


## [JB-Sat10-v2](https://www.lautsprecherforum.eu/viewtopic.php?t=4907)  
<img src="https://www.lautsprecherforum.eu/images/files/x_id_high_3_1967.jpg" alt="drawing" width="200"/> 

- Faital 10FE200 / Sica z009442 +Q07032B)  
- 96dB 1W/1m  
- 118dB (121dB Max / 124dB Peak) 
- 165W rms  
- 80Hz - 20,3kHz  
- 75x50°

changes:  

- 4 Ohm Faital 10FE200
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

## [PS-Bass V2](https://aw-audio.de/boxenbauplaene/PS-Bass%20MK2_.pdf)

- High efficiency
- still kinda portable


## Battery

I use Lipo battery packs from ALDI as they are cheap and light weight 

<img src="https://s7g10.scene7.com/is/image/aldi/202009080257?$H10-XL$" alt="drawing" width="200"/> 

- ca. 90wh
- high output power
- light

## Amplifier: [Wondom JAB5](https://store.sure-electronics.com/images/documents/4%20x%20100Watt%20Class%20D%20Audio%20Amplifier%20Board%20Integrated%20with%20DSP%20&%20BT%205.0%20-%20JAB5%20Datasheet.pdf)

- 2x TDA7498E: 2.1 mode (2 x 100W + 1 x 200W)
- Bluetooth APT-X HD
- DSP AUDAU1701

### DSP: [ADAU1701](https://www.analog.com/media/en/technical-documentation/data-sheets/ADAU1701.pdf)

The [Sure DSP Ratz IT Forum](https://suredsp.ratz-it.de/) provides all information for programming the DSP

- [Driver installation](https://suredsp.ratz-it.de/index.php?title=Treiber_installieren)
- [Programming](https://www.360customs.de/2015/01/sigmadsp-programmieren-sigma-studio-adau17011401a-eeprom-standalone-self-boot/ ) 

audio-filters/effects:

- [Psychoakustik & Psychoakustik-Effekte](https://curdt.home.hdm-stuttgart.de/PDF/Psychoakustik_und_Psychoakustik_Effekte.pdf)
- [dynamic-bass-boost-basics](https://ez.analog.com/dsp/sigmadsp/f/q-a/65338/dynamic-bass-boost-basics)
- [automaticspeakereq](https://wiki.analog.com/resources/tools-software/sigmastudio/toolbox/adialgorithms/automaticspeakereq)
- [fir filter guide](https://eclipseaudio.com/fir-filter-guide/)
## Box

idea: https://youtu.be/EEh01PX-q9I?t=2532 but flexibel 2k-PU is used -> cheaper than Decidamp

Sandwich poplar plywood-> 6mm plywood, ~1mm PU, 6mm plywood  
- stiff
- sounddamping
- light (ca. 3kg wood for the hole boy)

## Boxsim Simulation

![SPL](Simulation/SPL.jpg)
![Richtcharakteristik](Simulation/Richtcharakteristik.jpg)
