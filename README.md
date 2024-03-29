# hue-Bridge-Cube-for-homee

## Telegram Kanal 
 - https://t.me/homee_huecube

## Installation

Aktuelle Version des Chips ESP32 Wroom32 ( getestet auch mit M5Stack Core2 )

  - mit dem Esp Wlan Verbinden "hue_bridge_cube" 
  - anmelden an der WEBUI unter der IP 192.168.4.1 , Name admin und Passwort admin
  - Wlan Konfiguration öffnen und Wlan auswählen oder SSID eintippen und Passwort eingeben und speichern 
  - Cube neu starten und mit der IP oder hue-bridge-cube.fritz.box verbinden 
    ( wenn er an der Fritzbox angemeldet ist, ansonsten die Ip im Router raussuchen )
  - IP der Hue Bridge eintippen in der HUE Konfiguration
  - Gerätetypen (Mehrfachauswahl)  in der Liste auswählen und abspeichern
  - Button der Hue Bridge betätigen und dann den Neustart Button auf der WEBUI drücken
  - Esp WebUi öffnen, hier sollte jetzt stehen das der Stream zur HUE besteht und wieviele Geräte angelegt wurden
  - Wenn die Anzahl der Geräte stimmt dann diese Zahl in der HUE Konfiguration eingeben ( soll das vom Host gelöscht verhindern ) 
  - Automatisches starten des vhih Service aktivieren
  - in homee nun Geräte hinzufügen und homee in homee auswählen
    -> mit homee verbinden drücken -> IP Adresse xxx.xxx.xxx.xxx eingeben oder HueBridgeCube -> User XYZ -> PW ABC -> verbinden drücken
    nun sollten alle angelegten Geräte angezeigt werden
  - Aktuelles Update über die Seite IP/update einspielen
  - Aktuell getestet Zahl an angelernten Geräten liegt bei 47 Aktoren ( 167 Attribute ) ( Stand 4.12.2022 )
  - Löschen aller Userdaten über die WebUi möglich und über einen 7 fachen Powercut innerhalb von 5-7 Sekunden, danach startet der ESP mit offenen AP.
  - Wenn möglich den Hue Bridge nicht in ein Wlan Mesh einbinden, da es hier zu Problemen mit der Wlan Verbindung kommen kann.
  - Update für den Cube sollten nach Möglichkeit nicht über ein Applebrowser oder Endgerät aufgespielt werden, da es hier zu Problemen mit den Upload führen kann.
  - [optional] AP Passwort vergeben 
  - [optional] WEBUI Http Name  und Http Passwort neu vergeben, danach neu anmelden




# Update
17.03.2023 Version 1.4.7.Beta
- Blacklist hinzugefügt, gelöschte Geräte werden bei einem Neustart nicht mehr geladen.

16.01.2023 Version 1.4.6Beta2
- Fehlerbehebung wodurch es zum "vom Host gelöscht" kommen kann.
- der vhih Service kann jetzt in den Einstellungen automatisch oder manuell gestartet werden. (standard manuell)

25.12.2022 Version 1.4.6Beta1
- Anpassung bei der Speicherverwendung 
- Fehlerbehebung bei der Neueinrichtung die zum Neustart geführt hat

3.12.2022 Version 1.4.5
- kleine Anpassungen bei dem Speicherabruf 
- Fehlerbehebung bei der Intervallabfrage nach einem Neustart

16.11.2022 Version 1.4.5 Beta4
- in den Hue Einstellungen kann jetzt die Anzahl an Geräten angegegeben werden die beim Start vorhanden sein müssen 
  bevor der vhih Service gestartet wird. Sollte die Geräteanzahl nicht passen wird der Cube neu gestartet bis die entsprechende 
  Anzahl an Geräten vorhanden ist.
  Somit soll verhindert werden das es zu den  "vom Host gelöscht" Erscheinungen kommt.
  
23.10.2022 Version 1.4.5 Beta3
- In den Einstellungen kann jetzt ausgewählt werden ob ein Automatischer Abruf der Daten durchgeführt wird.
  
19.10.2022 Version 1.4.5 Beta2
- Die hue Bridge wird jetzt in einem Intervall von 30 Sekunden nach dem Zustand
  der Geräte gefragt (on/off, dimmen, zigbee Connection).
  Damit sollen Unstimmigkeiten der Aktoren gegenüber homee behoben werden.
  Geräte die in der Hue Bridge mit einem Sensor verknüpft sind,
  werden dann nach spätestens 30 Sekunden in homee richtig dargestellt.
  

17.10.2022 Version 1.4.5.Beta1
- Debug in den Werkseinstellungen zum Kontrollieren der Nachrichten von der Bridge.
- SSE Stream für den Browser eingebaut ( Apple mag das leider nicht so ) 

17.10.2022 Version 1.4.4
- Anpassungen aus der Beta enthalten
- Speicherfehler, der zum Absturz beim schalten vieler Lampen geführt hat, behoben.


30.09.2022 Version 1.4.4.Beta5
- Dimmwert angepasst
- Speicherbedarf etwas verringert 

27.09.2022 Version 1.4.4.Beta4
- Anpassungen an das Update der HueBridge Version BSB002|1.53.1953188020

23.09.2022 Version 1.4.4.Beta3
- Fehlerbehebung beim Verlust der Wlanverbindung ( Absturz )

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
 
  
  
  
