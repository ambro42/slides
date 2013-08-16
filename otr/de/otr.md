% Cryptoparty - Private Online-Gespräche mit OTR
% {{Name des Vortragenden}}
% {{Monat}} {{Tag}}, {{Jahr}}

# Cryptoparty
![](images/logo.png)

# Alice und Bob

- Alice und Bob wissen beide, wie man PGP benutzt.
- Beide kennen den öffentlichen Schlüssel des jeweils anderen.
- Sie möchten nicht die Tatsache verschleiern, dass sie miteinander gesprochen haben, sondern nur worüber sie gesprochen haben.
- Alice benutzt ihren öffentlichen Schlssel, um eine Nachricht zu signieren.
- Bob sollte wissen, mit wen er redet.
- Sie benutzt nun Bobs öffentlichen Schlüssel, um die Nachricht zu verschlüsseln.
- Niemand anderes als Bob kann die Nachricht lesen.
- Bob entschlüsselt sie und verifiziert die Signatur.
![](images/threat1.png)

# Überraschende Wendung

- Bobs Computer wurde vom FBI kompromittiert.
- Oder er ist nur mit einen Virus, einen Trojaner oder irgendwelcher Spyware infiziert.
- Bobs Schlüssel und Emails wurden abgegriffen.
- Entschlüsseln der alten Nachrichten
- Ihren Inhalt in Erfahrung bringen
- Herauslesen, dass sie von Alice gesendet wurden
- Und einen mathematischen Beweis haben, den man jedem anderen zeigen kann.
![](images/threat2.png)

# Was lief falsch?

- Das Programm erzeugte lauter belastende Hinweise
- Schlüsselmaterial das andere Daten entschlüsseln kann wurde über das öffentliche Internet gesendet
- Signaturen als Beweise, wer was gesagt hat
- Alice sollte besser aufpassen, was sie sagt
- Ihre Privatsphäre hängt an Bobs Taten

# Smalltalk und OTR

- Alice und Bob reden in einem Raum
- Niemand sonst kann zuhören
- Außer das Gespräch wird aufgezeichnet
- Niemand sonst weiß, über was sie reden
- Außer Alice oder Bob erzählen es weiter
- Niemand kann beweisen, was gesagt wurde
- Noch nicht einmal Alice oder Bob
- Diese Konversationen verlaufen "unter dem Radar", englisch “off-the-record”
- Es gibt Gesetze, die diese Art von Gesprächen schützen
- Es ist illegal, Gespräche ohne Einwilligung aufzuzeichnen
- Sie könnten sich auch am Telefon unterhalten
- Es ist illegal, Telefonleitungen anzuzapfen

# Perfect Forward Secrecy

- Kompromittierung von Schlüsseln sollte frühere Kommunikation nicht offen legen.
- Z.B. wenn Bobs Laptop geklaut wurde
- Benutze einen kurzlebigen Schlüssel zum verschlüsseln
- Wirf ihn nach der Benutzung weg
- Lösche ihn nachhaltig aus dem Speicher
- Benutze langlebige Schlüssel, mit deren Hilfe die kurzlebigen Schlüssel verteilt und authentisiert werden

# Repudiable Authentication

- Du kannst sicher sein, dass dein Gegenüber der ist, von dem du denkst.
- Privatsphäre kann nicht aufrechterhalten werden, wenn sich Angreifer als Freunde ausgeben
- Aber wir möchten keine digitalen Signaturen
- Non-repudiation bedeutet im Sicherheitskontext, dass es einen Beweis für Integrität und Ursprung der Daten gibt.
- Benutzt Message Authentication Codes (MACs)

# Verschlüsselung

- Niemand anderes kann deine Messaging-Nachrichten lesen, noch nicht einmal der Server

# Abstreitbarkeit

- Authentisierung mit gemeinsamem Schlüssel
- Alice und Bob haben den selben MK.
- MK wird benötigt um den MAC zu generieren.
- Bob kann nicht beweisen, dass Alice den MAC generiert hat, er hätte es ebenso sein können.
- Jeder, der eine Nachricht verifizieren kann, kann sie auch im Anschluss an eine Kommunikation fälschen und es so aussehen lassen, als ob sie von dir kämen.
- Also haben Nachrichten, die du gesendet hast keine digitalen Signaturen die von Dritten überprüft werden können (funktioniert nicht vor Gericht)
- Allerdings kann dein Gesprächspartner während der Konversation sicher sein, dass die Nachrichten die er sieht authentisch und unverändert sind.

# Was du benötigst

- Windows / Linux - pidgin mit dem OTR Plug-In. Lade zu erst pidgin auf pidgin.im herunter und dann das Plug-In von cypherpunks.ca/otr
- Mac OS - Lade adium von adium.im herunter (du brauchst kein zusätzliches Plug-In).

Es gibt auch Smartphone Apps, die OTR beherrschen:

- Android (Gibberbot).
- iOS (Chatsecure).

# Was mache ich als nächstes?

- Lege dir eine Adresse zu, damit Andere dich erreichen können.
- Finde die Person, mit der du sprechen möchtest. Baue Kontakt auf.
- Versteck dich unter dem Radar.
- Überprüfe die virtuellen Fingerabdrücke manuell, damit du sicher sein kannst, dass die Person die Richtige ist und du die Verschlüsselung starten kannst.
- Stelle sicher, dass Log-Aufzeichnung in deinem Chatprogramm ausgeschaltet ist!
- Stelle sicher, dass die Person mit der du sprechen möchtest das selbe tut!
- Macht ein gemeinsames Geheimnis aus, an dem ihr euch erkennen könnt.
- Das war's! Denke daran, die Chat-Sitzung zu beenden und alle Fenster zu schließen wenn du mit dem Chat fertig bist.

# Was OTR leisten kann und was nicht

Pros:

- Sicherheit
- Funktioniert auf vielen Geräten.
- Wenn man es einmal eingerichtet hat, ist es ziemlich einfach zu benutzen.

Kontras:

- Beide Gesprächspartner müssen online sein.
- Man kann einen sicheren Chat nur zwischen zwei Menschen einrichten.
- Dsa Gespräch ist nur sicher während es gerade statt findet. Wenn du Logs speicherst, werden sie nicht verschlüsselt sein.

# Nun zu dir :)

- Nun installieren wir Pidgin, Adium oder Bitlbee auf deiner Windows-, Mac- oder Linux-Maschine.
- Gibberbot unter Android oder Chatsecure unter iOS.

Was du tun solltest, sobald das Programm installiert ist:

- Stelle sicher, dass du weißt was ein Fingerprint ist und wo du deinen findest.
- Stelle sicher, dass du weißt wie man den Fingerprint eines Anderen überprüfst.
- Stelle sicher, dass du weißt wie du das Logging in deinem Chat-Programm ausstellst.
- Teste alles, indem du mit einem neuen Freund von der CryptoParty einen sicheren Chat durchführst.

# Howto: pidgin und pidgin-otr unter Ubuntu/Debian installieren
![](images/pidgin.png)

Mit root-Rechten:

- apt-get install pidgin pidgin-otr

# Howto: Pidgin + OTR Plugin unter Windows installieren

![](images/pidgin.png)

- Gehe auf http://www.pidgin.im/download/windows
- Klicke auf den "Download Pidgin for Windows"-Link
- Speichere die Installationsdatei, dann öffne sie und installiere.
- Gehe auf http://www.cypherpunks.ca/otr
- Klicke den "Win32 installer for pidgin"-Link im "OTR plugin for Pidgin"-Bereich
- Speichere die Installtionsdatei, dann öffne sie und installiere.
- Nachem du pidgin und das OTR-Plugin erfolgreich installiert hast, kannst du die Installationsdateien von deinem Computer löschen.
- Starte pidgin. Aktiviere das OTR-Plugin unter Werkzeuge -> Plugins. Setze ein Häkchen in der Box "Off-the-record Messaging" um das Plugin zu aktivieren.

# Howto: Adium unter Mac installieren
![](images/adium.jpg)

- Gehe auf http://adium.im/ und lade Adium herunter.
- Adium hat OTR bereits vorinstalliert.
- Speichere die Installtionsdatei, dann öffne sie und installiere.
- Nachdem du Adium erfolgreich installiert hast, kannst du die Installationsdateien von deinem Computer löschen.
- Starte Adium.

# Einen Jabber-Konto unter jabber.ccc.de registrieren

- Starte Pidgin.
- Richte dein Konto ein. (Konten > Hinzufügen/Ändern > Hinzufügen)
- Protokoll: XMPP
- Benutzername: [Was du möchtest!] 
- Domain:   jabber.ccc.de
- Passwort: [Was du möchtest!] 
- Setze ein Häkchen bei "Als neues Konto auf dem Server anlegen"

# Einen verschlüsselten Chat starten

- Füge einen Kontakt hinzu
- Starte einen Chat mit diesem Kontakt.
- Klicke auf "nicht verifiziert".
- Wähle "Manueller Fingerprint-Vergleich".
- Bringe deinen Freund dazu, dir den Fingerprint zuzusenden oder persönlich zu zeigen.
- Lass sie den selben Vorgang für dich durchführen.

# Links
- http://www.pidgin.im/
- http://adium.im/
- http://bitlbee.org/
- http://www.cypherpunks.ca/otr/
- https://en.wikipedia.org/wiki/Off-the-Record_Messaging

# Fragen?

