# hue-Bridge-Cube-for-homee

## Installation

Aktuelle Version des Chips ESP32 Wroom32 

  - mit dem Esp Wlan Verbinden "hue_bridge_cube" ohne PW oder homee-community-cube
  - anmelden an der WEBUI unter der IP 192.168.4.1 , Name admin und Passwort admin
  - Wlan Zugangsdaten eintippen
  - AP Passwort vergeben 
  - WEBUI Anmeldenamen und Passwort neu vergeben, danach neu anmelden
  - IP der Hue Bridge eintippen
  - Gerätetypen (Mehrfachauswahl)  in der Liste auswählen und abspeichern
  - Button der Hue Bridge betätigen und dann den Neustart Button drücken
  - Die Anmeldung an der Hue Bridge wird durchgeführt
  - Esp unter hue-bridge-cube.fritz.box aufrufen ( wenn er an der Fritzbox angemeldet ist, ansonsten die Ip im Router raussuchen )
    hier Sollte jetzt stehen das der Stream zur HUE besteht und wieviele Geräte angelegt wurden
  - in homee nun Geräte hinzufügen und homee in homee auswählen
    -> mit homee verbinden drücken -> IP Adresse xxx.xxx.xxx.xxx eingeben oder HueBridgeCube -> User XYZ -> PW ABC -> verbinden drücken
    nun sollten alle angelegten Geräte angezeigt werden
  - Aktuelles Update über die Seite IP/update einspielen
  - Aktuell getestet Zahl an angelernten Geräten liegt bei 40 Aktoren ( Stand 16.7.22 )
  - Löschen aller Userdaten über die WebUi möglich und über einen 7 fachen Powercut innerhalb von 5-7 Sekunden, danach startet der ESP mit offenen AP.
  - Wenn möglich den Hue Bridge nicht in ein Wlan Mesh einbinden, da es hier zu Problemen mit der Wlan Verbindung kommen kann.
  - Update für den Cube sollten nach Möglichkeit nicht über ein Applebrowser oder Endgerät aufgespielt werden, da es hier zu Problemen mit den Upload führen kann.
  




# Update

22.09.2022 Version 1.4.4.Beta2
- Das Händling des Stream und Request wurden angepasst um Speicherplatz
  nach dem Erhalt der Nachricht frei zu geben.

19.09.2022 Version 1.4.4.Beta1
- Fehlerbehebung bei der 1.4.3


18.09.2022 Version 1.4.3
- Autostart bei fehlender Verbinung zur Hue hinzugefügt.
- kleiner Fehler beseitigt
  

11.09.2022 Version 1.4.3.Beta3
- In der Hue Konfiguration können jetzt angelegt vhih Geräte einzeln gelöscht werden.
  - Attributeanzahl wird aktuell nicht angepasst nach dem löschen.

05.09.2022 Version 1.4.3.Beta2

- Fehler beim Wlanverlust behoben
- nach dem wiederherstellen der Verbindung zum Wlan wird jetzt der Stream zur Hue sauber neu gestartet
- Verbindungsabruch wird gezählt und angezeigt

03.09.2022 Version 1.4.3.Beta

- Bug beim reconnect des Wlan entfernt wodurch das Anmelden an einer neuen Installation ( AP Mode)  immer nach 30 Sekunden neu gestartet wurde.
- Anzeige der Laufzeit des Cube ohne Neustart hinzugefügt 

02.09.2022 Version 1.4.2

- WiFi Reconnect hinzugefügt
- Captiv für LocalenAP hinzugefügt ( Windows , mit Apple gibt es Probleme beim öffnen der Seite )
- HueBridge kann über die WebUi in den Anlernmodus versetzt werden und für 40 Sekunden können neue Geräte
  angemeldet werden ohne die Hue App nutzen zu müssen.
- Restart bei fehlenden HueKey wurde abgestellt, somit sollte die WebUi dann auch erreichbar bleiben

21.08.2022 Version 1.4 

- Name des HueBridgeCube kann jetzt geändert werden
- neue WebUi mit Verknüpfung zur Updateseite
  - Fehlerbehebung beim speichern von Werten,
    es wird nicht mehr auf die Hauptseite gesprungen sondern man verbleibt auf der Eingabeseite
    
- Behandlung der Switche wurde verändert, damit die Verzögerung für das Einschalten entfällt
- Neue Geräte hinzugefügt
  - Hue Tap Dial Switch
  - Hue Smart Button
  - Hue InWall Modul

19.08.2022 Version 1.4.Beta2

- neue WebUi mit Verknüpfung zur Updateseite
- Behandlung der Switche wurde verändert, damit die Verzögerung für das Einschalten entfällt

18.08.2022 Version 1.4.Beta

- Neue Geräte hinzugefügt
  - Hue Tap Dial Switch
  - Hue Smart Button
  - Hue InWall Modul
  
17.08.2022 Version hue2test.1.3.9
- Testversion für die Verwendung von zwei ESP an einem homee ( 2 vhih mit gleichen Namen funktionieren nicht )
  daher die Testversion für den 2.ESP. 

13.08.2022 Version 1.3.9.1.beta
- Gruppen haben jetzt einen Rückkanal von der Hue Bridge
- FT55 Friends of Hue werden jetzt unterstützt

30.07.2022 Version 1.3.9
- Gerätetypen die angelernt werden sollen können in der WebUi ausgewählt werden

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
  - Hue Tap Dial Switch
  - Hue Smart Button
  - Hue InWall Modul
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
  - TRADFRI GU10 CWS 345lm
  - Tint E14 white+color 6W + 4,9 W Version
  - Tint E27 white+color 9,5 W + 9 W Version
  - Tint 3er Unterbauleuchte Armaro White
  - Tint GU10 white+color 6W
  - Tint Talpa white+color (Lightbar)
  - Tint Smart Power Strip (4-Fach Steckdosenleiste)
  - Tint Inwall Modul Smart Switch
  - Vimar Friends of Hue Smart Switch FT55 
 
  
  
  
