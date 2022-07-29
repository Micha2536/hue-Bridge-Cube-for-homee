# hue-Bridge-Cube-for-homee

## Installation

Aktuelle Version des Chips ESP32 Wroom32 

  - mit dem Esp Wlan Verbinden "hue_bridge_cube" ohne PW 
  - anmelden an der WEBUI unter der IP 192.168.4.1 , Name admin und Passwort admin
  - Wlan Zugangsdaten eintippen
  - AP Passwort vergeben 
  - WEBUI Anmeldenamen und Passwort neu vergeben, danach neu anmelden
  - IP der Hue Bridge eintippen
  - Button der Hue Bridge betätigen und dann den Neustart Button drücken
  - Die Anmeldung an der Hue Bridge wird durchgeführt
  - Esp unter hue-bridge-cube.fritz.box aufrufen ( wenn er an der Fritzbox angemeldet ist, ansonsten die Ip im Router raussuchen )
    hier Sollte jetzt stehen das der Stream zur HUE besteht und wieviele Geräte angelegt wurden
  - in homee nun Geräte hinzufügen und homee in homee auswählen
    -> mit homee verbinden drücken -> IP Adresse xxx.xxx.xxx.xxx eingeben oder HueBridgeCube -> User XYZ -> PW ABC -> verbinden drücken
    nun sollten alle angelegten Geräte angezeigt werden
  - Aktuelles Update über die Seite IP/update einspielen
  - Aktuell getestet Zahl an angelernten Geräten liegt bei 40 Aktoren ( Stand 16.7.22 )





# Update
27.07.2022 Verson 1.3.8.1Beta2
- Gruppen und Zonen integriert , Rückkanal noch nicht integriert  
- neue WebUi

24.07.2022 Version 1.3.8
- WEBUI ist nun passwortgeschützt
- WLAN AP kann passwortgeschützt werden
- Updateseite passwortgeschützt
- neu angelernte Geräte ( Lights ) an der Hue Bridge werden automatsich angelegt und stehen im homee zur Verfügung
- sollte das System starten und keine Geräte angelernt werden können wird nach einem Zeitintervall neugestartet
- Userdaten können in der WEBUI gelöscht werden
- wenn man die Zugangsdaten nicht mehr weiß, kann mit einem 7 maligen Powercut kurz nacheinander ( abstand der Powercut ca. 1 Sekunde )
  alle Daten zurücksetzenn und der Cube (ESP) öffnet wieder sein ungeschützten WLAN AP 
  

16.07.2022 Version 1.3.6
- Inwall Modul hinzugefügt
- Name des vhih auf HueBridgeCube geändert, Anlernen nicht mehr mit IP nötig sondern über den Namen
- Nicht anlernbare Geräte werden gespeichert
- Abfrage der Deviceliste stabiler ausgeführt

02.07.2022 Version 1.2.8
- Fehlerbehebung beim AP und PW hinzugefügt
- Hue Bewegungsmelder hinzugefügt mit Motion, Lux und Temp

29.06.2022 Version 0.6.2.1
  - Löschen des Hue Token in der Config möglich
  - Fehlerbehebung bei dem Update der vhih Attribute die zum Absturz des vhih geführt haben

29.06.2022 Version 0.6.2
  - Anzeige in der Config ob der Stream zur HUE Bridge aufgebaut wurde 
  - Anzeige der angelegten vhih Geräte 

29.06.2022 Version 0.6.1
  - Unterstützung des Farbkanal über hue
  - IP des Cube wird in der Config angezeigt
  - Netzwerkname = hue-bridge-cube
  - in der FritzBox ist er dann unter hue-bridge-cube.fritz.box erreichbar 



# Getestete Geräte
  - Hue Dimmer Switch V1 und V2 ( aktuell nur Singleclick umgesetzt )
  - Hue Iris 
  - Hue lightstrip plus
  - Hue color lamp LCT007
  - Hue Motion Sensor und Outdoor 
  - Hue Aurelle Panel
  - Hue color pendant up
  - Hue color pendant down
  - Hue go
  - Hue color Candle (e14)
  - Hue Wihte lamp
  - Hue Ambiente ceiling
  - Hue smart Plug
  - Innr RB 285 C
  - Innr RB 278 T
  - Innr SP 120
  - Innr SP 220
  - Innr Flex Light Color,FL 120 C
  - Innr Smart Puck white
  - Immax IM-Z3.0-RGBW
  - Osram LIGHTIFY Outdoor Flex RGBW
  - Osram CLA 60 TW Bulb 
  - Osram Plug
  - Paul Neuhaus Q-VITO 
  - Paulmann 
  - TRADFRI Driver 30W 
  - TRADFRI Driver 10W
  - Tint E14 white+color 6W + 4,9 W Version
  - Tint E27 white+color 9,5 W + 9 W Version
  - Tint 3er Unterbauleuchte Armaro White
  - Tint GU10 white+color 6W
  - Tint Talpa white+color (Lightbar)
  - Tint Smart Power Strip (4-Fach Steckdosenleiste)
  - Tint Inwall Modul Smart Switch
 
  
  
  
