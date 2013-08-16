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

- You are assured the correspondent is who you think it is.
- Can’t maintain privacy if attackers can impersonate friends
- But we do not want digital signatures
- Non-repudiation in digital security means that there is proof of the integrity and origin of data.
- Use Message Authentication Codes (MACs)

# Encryption

- No one else can read your instant messages, not even the server

# Deniability

- Shared key authentication.
- Alice and Bob have same MK.
- MK required to compute MAC.
- Bob cannot prove that Alice generated the MAC, he could have done it, too.
- Anyone who can verify can also forge messages after a conversation to make them look like they came from you.
- So messages you send do not have digital signatures that are checkable by a third party. (Doesn't work in court)
- However, during a conversation, your correspondent is assured the messages he sees are authentic and unmodified. 

# What you need

-  Windows / Linux - pidgin with OTR plug-in. Download pidgin first from pidgin.im and then the plug in from cypherpunks.ca/otr

- Mac OS - download adium from adium.im (you don't need an additional plug in).

There are also OTR enabled smartphone apps

- Android (Gibberbot).
- iOS (Chatsecure).

# Then what do I do?

- Set up an address for people to reach you at.

- Find the person you want to speak to. Make contact.

- Go off the record.

- Manually verify fingerprints to be sure it is who you think it is and to enable encryption.

- Make sure logging is disabled in your chat client's settings!

- Make sure to also ask the person you want to speak to do the same!

- Discuss a shared secret to authenticate your conversation partner with.

- That's it! Remember to end the chat session and close any open windows when you are done chatting.

# What OTR can do and what it can't

Pros:

- Secure
- Works on a number of devices.
- Once you've set it up, it's pretty easy to use.

Cons:

- You both have to be online.
- And it is both. You can only have two in a secure chat.
- The conversation is only secure while its happening. If you keep logs, they won't be encrypted.

# Over to you :)

-  Now let's install Pidgin, Adium, or Bitlbee on your PC, Mac or Linux machine.

- Gibberbot on Android or Chatsecure on iOS.

Things to do once program is intalled:

- Ensure you know what a fingerprint is and how to find yours.
- Ensure you know how to verify someone elses fingerprint.
- Ensure you know how to turn your chat client's logging setting off.
- Test by having an encrypted chat with a new friend at the Cryptoparty.

# Howto: install pidgin and pidgin-otr on Ubuntu/Debian
![](images/pidgin.png)

as root:

-  apt-get install pidgin pidgin-otr

# Howto: install Pidgin + OTR plugin on Windows

![](images/pidgin.png)

- Goto http://www.pidgin.im/download/windows
- Click the Download Pidgin for Windows link
- Save the installation file, then navigate to it and double click it. Install it.
- Goto http://www.cypherpunks.ca/otr
- Click the Win32 installer for pidgin link in the OTR plugin for Pidgin section
- Save the installer, then navigate to it and double click it. Install it.
- After you have successfully installed Pidgin and OTR you may delete the installation programs from your computer.
- Run Pidgin. Enable the OTR plugin: OTR: Tools -> Plugins. Check the Box "off the record messaging" to enable the plugin.

# Howto: install Adium on Mac
![](images/adium.jpg)

- Goto http://adium.im/ and download Adium.
- Adium comes with otr preinstalled.
- Save the installation file, then navigate to it and install it.
- After you have successfully installed Adium you may delete the installation files from your computer.
- Run Adium.

# Getting a jabber account with jabber.ccc.de

- Run Pidgin.
- Setup your chat account. (Accounts > Manage Account > Add)
- Protocol: XMPP
- Username: [whatever you like!] 
- Domain:   jabber.ccc.de
- Password: [whatever you like!] 
- Check 'create this new account on the server'

# Starting An Encrypted Chat

- Add a Buddy
- Start Chatting with a buddy.
- Click on "Not Verified"
- Use Manual Fingerprint Verification.
- Get your buddy to send you their fingerprint or show you in person.
- Let them do the same for you.

# Links
- http://www.pidgin.im/
- http://adium.im/
- http://bitlbee.org/
- http://www.cypherpunks.ca/otr/
- https://en.wikipedia.org/wiki/Off-the-Record_Messaging

# Questions?

