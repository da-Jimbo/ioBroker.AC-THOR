# Einbindung des MyPV AC•THOR in ioBroker über den ioBroker Modbus-Adapter. #

<img src="https://user-images.githubusercontent.com/819464/50492875-5e5b9b00-0a1a-11e9-8808-5a3a764bc999.jpg"></img>

## my-PV AC•THOR ##

AC•THOR ist ein 0 - 3 kW (6 kW) stufenlos geregelter PV/BHKW Power-Manager für
Warmwasser, elektrische Wärmequellen und optional Heizung.

Durch vielfältige Konfigurationsmöglichkeiten sind mehrere Anwendungsszenarien denkbar.

Ausgiebige Informationen findet man auf https://www.my-pv.com/de/produkte/ac-thor sowie im Handbuch.

So ist es stufenlos möglich bis zu 6 kW über 2 Heizstäbe (zB. je 1 im Warmwasserpuffer und 1 im Brauchwasserpuffer) überschüssige Energie für die Warmwasser-Bereitung und Heizung
zur Verfügug zu stellen.

Durch die stufenlose Regelung kann die Einspeiseleistung theoretisch bis gegen Null ausgeregelt werden.

Sie kann mit Heizstäben in Warmwasser- und oder Pufferspeicher oder auch direkt mit zB. Infrarotheizpanelen verwendet werden.


Die Anbindung an ioBroker erfolgt dabei über den Modbus Adapter
(Dank an Bluefox für den tollen Adapter!)

# 1. Schritt

  Installation des Modbus Adapter.

  Bitte im ioBroker Admin unter Adapter den Modbusadapter auswählen und mit einem Klick auf das "+" Symbol hinzufügen.

# 2. Schritt

  Grundparameter Modbus einstellen

  Nach der Installation des Adapters landen wir automatisch im Konfigurationsmenue.
  Hier bitte die IP-Adresse des AC•THOR eingeben und die anderen Werte wie im Bild ersichtlich einstellen.

  <img src="https://github.com/da-Jimbo/ioBroker.AC-THOR/blob/master/Parameter1.png"></img><img src="https://github.com/da-Jimbo/ioBroker.AC-THOR/blob/master/Parameter2.png"></img>

# 3. Schritt

   unter dem Reiter Holding-Register den Inhalt der Datei Holding_registers.csv einfügen
   
   <img src="https://github.com/da-Jimbo/ioBroker.AC-THOR/blob/master/TSV.png"></img>

  und mit Import bestätigen.

Mit Speichern und Schließen wird die Instanz gestartet.


# 4. Inbetriebnahme und Regelung

Werte können z.B. per Blockly in den Datenpunkt geschrieben werden.(alle 10sek.)

<img src="https://github.com/da-Jimbo/ioBroker.AC-THOR/blob/master/Wertschreiben.png"></img>






## Changelog

  ### 1.0.0 (09.03.2024)
* da-Jimbos Version.

  ### 0.1.0 (25.12.2018)
* First (Initial) Version.


## License
The MIT License (MIT)

Copyright (c) 2018 Jedo <nospam@biglinux.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
