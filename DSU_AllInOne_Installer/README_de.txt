Hi,

DSU Automatisierung zur Installation von GSI/System Images 
im Format xz,zip,img,md5 mit 2 Examples bei erhalt der Geräte Garantie.

About,
Dynamic System Updates (DSU)

Dynamic System Updates (DSU) ist eine in Android 10 eingeführte Systemfunktion, die hat folgendes:

    -Laden Sie ein neues GSI (oder ein anderes Android-Systembild) auf Ihr Gerät.
    -Erzeugt eine neue dynamische Partition.
    -Loads lud die heruntergeladene GSI auf die neue Partition.
    -Starten Sie die GSI als Gast-Betriebssystem auf dem Gerät.

Mit DSU können Sie auch einfach zwischen dem aktuellen Systembild und dem GSI wechseln, damit Sie die System/GSI ausprobieren können, ohne die Korruption des aktuellen Systembildes zu riskieren.


DSU Anforderungen

DSU ist abhängig von dem Android Dynamic Partition Feature und erfordert die GSIs von Google oder Ihren OEMs als vertrauenswürdiges Systembild signiert sind. (es können auch CustomROM GSI/System Images mit diesem verfahren verwendet werden)

DSU ist eine Funktion des Herstellers Ihres Geräts. Lesen Sie Ihr Gerät Hersteller Support-Seite zur Verfügbarkeit. Google hat DSU auf Pixel aktiviert & neuere Geräte seit Android 10 Beta 4 Integriert.



Hier habe ich ein paar Tools geschrieben die die jeweilige Resource in das DSU Format bringt und dann die Installation
auf den Device startet.
Dazu einfach das System Image oder GSI in den Ordner Kopieren und die jeweilige Anwendung starten, achtet darauf das das
Gerät via USB-Kabel Verbunden ist.
Ihr könnt verwenden xz,zip,md5,img System Images.
Das Faszinierende daran ist ihr Unlockt zwar den Bootloader aber er wird nicht mit Custom Files geFlasht somit, bleibt die 
Garantie erhalten.
Als Beispiel habe ich beigefügt Android 13 LineageOS mit SuperSu und Googles Android 14 Beta GSI, beide laufen einwandfrei,
damit ist dies der Anfang der Installation von CustomROMs bei erhalt der Garantie ohne ROOT Rechte oder Custom Recovery.

DSU ist eine Android Funktion die in den Entwickler Optionen versteckt ist, also Systemeigen.


Was muss ich tun?
#################


0# zu Allererst eine Backup mit SmartSwitch anlegen den die daten werden im folgenden Schritt gelöscht

1# Es benötigt einen geöffneten Bootloader, damit die GSI ROMs starten können (Garantie bleibt erhalten)
   -Aktiviert Entwickler Optionen wie folgt
   -Telefoninformationen>>Softwareinformationen
   -7 mal hintereinander "Buildversion" tippen und mit Entsperrcode bestätigen
   -unter Einstellungen nun Entwickler Optionen öffnen
   -die 2 Funktionen Aktivieren (oem-unlock/bootloader-unlock),(usb-debugging)
   -danach das handy ausschalten und USB-Kabel mit PC/Handy verbinden
   -nun mit VOL+ & VOL- & Power Tasten in den Download Modus starten
   -im Download Modus VOL+ solange drücken bis das nächste Menu erscheint
   -nun mit VOL+ bestätigen und der Bootloader ist Unlockt (ACHTUNG DATEN WERDEN GELÖSCHT)
   
2# Nun das Android System erstmal erneut Einrichten
   -Daten wiederherstellen mit SmartSwitch
   -Entwickler Option erneut Aktivieren und "USB-Debugging" Aktivieren

3# Jetzt könnt ihr euch eines der Anwendungen aussuchen um eure geDownloadeten CustomROMs zu Installieren
   falls die benachrichtigung USB-Debugging zulassen erscheint, bitte dauerhaft zulassen
   und dann erlauben drücken.
   Nun die Anwendung erneut Starten und es funktioniert
   nun noch den Entsperrcode bei Aufforderung für "Dynamic System Update" eingeben, 
   schon beginnt die Installation.
   
4# Ist die Installation Abgeschlossen Bitte Anleitung.jpeg anschauen

5# Nun könnt ihr zwischen den 2 Betriebssystemen wechseln so oft ihr wollt.



GSI CustomROM Quellen

AndyYans GSI
https://sourceforge.net/projects/andyyan-gsi/files/

Sourceforge.net GSIs
https://sourceforge.net/directory/gsis/windows/

Generic System Image list
https://github.com/phhusson/treble_experimentations/wiki/Generic-System-Image-%28GSI%29-list

Google Android GSI
https://developer.android.com/topic/generic-system-image/releases

Samsung STOCKROM Firmware Website
https://samfw.com/

phhusson GSI list
https://magiskzip.com/gsi-list-phhusson/

Android ROM list
https://github.com/musabcel/android_rom_list