# DNMS (Digital Noise Measurement Sensor)

Ein Sensor-Modul zur Schallpegelmessung. Es wird neben dem LAeq-Wert über einem Zeitintervall auch der min. und max. LA-Wert in diesem Zeitintervall festgehalten. Das zentrale Element des DNMS ist ein digitales MEMS-Mikrofon (InvenSense ICS-43434). Ein Mikrocontroller-Board (Teensy3.6 / Teensy4.0) übernimmt die digitalen Daten vom Mikrofon über die I²S Schnittstelle als  16-Bit, 44,1 kHz PCM Daten.  Die Audiodaten werden über einen digitalen A-Filter bewertet, dann wird der Effektivwert bestimmt und daraus der Schalldruckpegel entsprechend der Mikrofonsensitivität berechnet. Die einzelnen Schalldruckpegelwerte werden zu einem fortlaufenden LAeq-Wert weitergerechnet. Ebenso werden der max. und min. Schalldruckpegel (LAmax, LAmin) aus dem Intervall abgespeichert.

Die Werte werden dann über eine I²C-Schnittstelle an einen abfragenden Mikrocontroller zur Weiterverarbeitung übertragen. Das Abfrage-Intervall kann 1 Sekunde betragen oder auch bis zu 3600 Sekunden.

Geplante Erweiterungen sind zusätzlich zur A-Bewertung eine C-Bewertung d.h. Bildung von LCeq, LCmax und LCmin, sowie eine FFT zur weiteren Analyse im Frequenzbereich.


## Neuigkeiten

### August 2020: Neue PCBs verfügbar
- Airrohr-PCB-V1.4
- DNMS-T3.6-V1.4
- DNMS-T4.0-V1.4
- DNMS-T4.0+NodeMCU-V1.4

### Juni 2020: Teensy4.0 läuft stabil und wird nun empfohlen
- Teensy4.0 ist preiswerter als Teensy3.6
- Teensy4.0 ist leistungsfähiger als Teensy3.6
- Teensy3.6 wird weiter unterstützt




----------------------------------------------------------------------------------------------------------------


A sensor modul for SPL measurement. Over a period of time the LAeq value is calculated, beside that the minimal and the maximal LA value is covered over the time period. The central element of DNMS is a digital MEMS-Microphone (InvenSense ICS-43434). The digital data is fed from the microphone via a I²S connection as 16-bit, 44,1 kHz PCM data to a microcontroller board (Teensy3.6 / Teensy4.0). The data is filtered by an A-filter, then the RMS value is calculated. Further the sound pressure level (SPL) is calculated based on microphone sensivity. The SPL values are integrated over time to give the LAeq. Also the maximum level in the measurement period LAmax and the minimum level LAmin will be kept.

All measurements will be transfered to a further microcontroller via I²C bus. The intervall time to pick up measurements can reach from 1 second up to 3600 seconds.

Planned extensions are an additional C-filter to get LCeq, LCmax and LCmin and further FFT for analysis in the frequency domain.


## News

### August 2020: New PCBs are available
- Airrohr-PCB-V1.4
- DNMS-T3.6-V1.4
- DNMS-T4.0-V1.4
- DNMS-T4.0+NodeMCU-V1.4

### June 2020: Teensy4.0 is stable and now recommended
- Teensy4.0 is cheaper than Teensy3.6
- Teensy4.0 has a lot more power than Teensy3.6
- Teensy3.6 will be further supported



