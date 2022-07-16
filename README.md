# hue-Bridge-Cube-for-homee

## Installation

Aktuelle Version des Chips ESP32 Wroom32 

  - mit dem Esp Wlan Verbinden "hue_bridge_cube"
  - Wlan Zugangsdaten eintippen
  - IP der Hue Bridge eintippen
  - Button der Hue Bridge betätigen und dann den Neustart Button drücken
  - Die Anmeldung an der Hue Brige wird durchgeführt
  - Esp unter hue-bridge-cube.fritz.box aufrufen ( wenn er an der Fritzbox angemeldet ist, ansonsten die Ip im Router raussuchen )
    hier Sollte jetzt stehen das der Stream zur HUE besteht und wieviele Geräte angelegt wurden
  - in homee nun Geräte hinzufügen und homee in homee auswählen
    -> mit homee verbinden drücken -> IP Adresse xxx.xxx.xxx.xxx eingeben -> User XYZ -> PW ABC -> verbinden drücken
    nun sollten alle angelegten Geräte angezeigt werden





# Update

02.07.2022 Versin 1.2.8
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
  - Hue Dimmer Switch V1 und V2
  - Hue Iris 
  - Hue lightstrip plus
  - Hue color lamp LCT007
  - Hue Motion Sensor und Outdoor
  - Hue Aurelle Panel
  - Hue color pendant up
  - Hue color pendant down
  - Hue go
  - Innr RB 285 C
  - Innr RB 278 T
  - Innr SP 120
  - Innr SP 220
  - Innr Flex Light Color,FL 120 C
  - Immax IM-Z3.0-RGBW
  - Osram LIGHTIFY Outdoor Flex RGBW
  - Osram CLA 60 TW Bulb 
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
 
  
  
  
