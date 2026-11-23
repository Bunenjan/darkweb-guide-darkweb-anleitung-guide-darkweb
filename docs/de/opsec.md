# Weiterführende Sicherheit, OpSec und Praxis-Tipps

[← Zurück zur Übersicht](../../README.de.md)

Der Tor Browser schützt deine Verbindung. Echte Anonymität hängt aber vor allem von deinem Verhalten ab. Hier findest du typische Anfängerfehler, wichtige Funktionen wie Tor Bridges und den Unterschied zu spezialisierten Betriebssystemen.

## 1. Typische OpSec-Fallen vermeiden

- **Fenstergrösse nicht verändern:** Der Tor Browser startet absichtlich mit einer standardisierten Fenstergrösse. Webseiten können über die Fenster- oder Bildschirmgrösse dein Gerät wiedererkennen (*Browser-Fingerprinting*). Der Tor Browser schützt davor mit **Letterboxing**: Er fügt graue Ränder hinzu und verbirgt so die echte Fenstergrösse. Trotzdem ist die Standardgrösse am sichersten. Also das Fenster nicht maximieren und nicht im Vollbild surfen.
- **Kein VPN zusätzlich zu Tor:** Das Tor-Projekt rät grundsätzlich davon ab, ausser man ist fortgeschritten und weiss genau, wie man beides richtig einrichtet. Ein VPN-Anbieter kennt deine echte IP-Adresse und meist deine Zahlungsdaten. Du verlagerst das Vertrauen also nur auf eine Firma. Wenn du verbergen willst, dass du Tor nutzt, verwende **Tor Bridges** (Abschnitt 3).
- **Metadaten in Dateien beachten:** Fotos enthalten oft EXIF-Daten wie Kameramodell oder GPS-Koordinaten, Dokumente oft Autor und Bearbeitungszeit. Am sichersten: keine eigenen Dateien teilen. Sonst die Metadaten vorher entfernen, zum Beispiel mit dem Programm *MAT2*.
- **Keine Gewohnheiten übernehmen:** Verwende im Tor Browser nie denselben Benutzernamen, dasselbe Passwortmuster oder dasselbe Profilbild wie im normalen Internet (Clearnet).

## 2. Tor Browser, Tails oder Whonix?

| Lösung | Wie es funktioniert | Wann sinnvoll? |
| --- | --- | --- |
| **Tor Browser** | Normale App auf Windows, macOS, Linux oder Android. | Für privates Surfen und Recherchen. Kann aber Spuren auf dem Hauptsystem hinterlassen, und Schadsoftware auf dem Gerät gefährdet auch den Browser. |
| **Tails** | Eigenes Betriebssystem, startet vom USB-Stick und vergisst beim Herunterfahren alles (*amnesisch*). | Wenn dein Computer nicht ganz vertrauenswürdig ist oder keine Spuren auf der Festplatte bleiben dürfen. |
| **Whonix** | Zwei virtuelle Maschinen (Gateway und Workstation), die den ganzen Netzwerkverkehr zwingend über Tor leiten. | Für Fortgeschrittene, die maximalen Schutz vor IP-Leaks durch Schadsoftware oder Programmfehler wollen. |

## 3. Blockaden umgehen mit Tor Bridges

Manche Internetanbieter, öffentliche WLANs (z. B. in Hotels, Schulen oder Zügen) oder Länder blockieren Verbindungen zum Tor-Netzwerk. Dann helfen **Bridges**: Tor-Eingangsserver, deren Adressen nicht öffentlich sind.

1. Im Tor Browser die **Settings** öffnen und links **Connection** wählen.
2. Zum Abschnitt **Bridges** scrollen.
3. Auf **Select a Built-In Bridge** klicken und einen Typ wählen:
    - **obfs4:** tarnt den Tor-Verkehr als zufälligen Datenstrom.
    - **Snowflake:** leitet die Verbindung über Proxys von Freiwilligen. Gut bei strengen Sperren.
4. Mit **OK** bestätigen. Die Einstellung wird gespeichert, sobald du den Tab schliesst.

Beim allerersten Start geht es auch über **Configure Connection** im Startfenster.

## 4. Echte Seiten erkennen

Im Darkweb gibt es keine Zertifizierungsstellen wie im normalen Web. Betrugsseiten kopieren bekannte Dienste mit leicht veränderten .onion-Adressen.

- **Nur offizielle Quellen:** .onion-Adressen nie aus Social Media, Foren oder unmoderierten Wikis übernehmen. Immer über die normale Webseite des Anbieters gehen, z. B. über den Knopf ".onion available", oder die Liste [Real-World Onion Sites](https://github.com/alecmuffett/real-world-onion-sites) nutzen.
- **PGP-Signaturen:** Manche Anbieter veröffentlichen ihre .onion-Adresse oder wichtige Nachrichten zusätzlich mit einer **PGP-Signatur** (*Pretty Good Privacy*). Mit Programmen wie *GnuPG* oder *Kleopatra* kannst du prüfen, ob eine Nachricht wirklich vom echten Betreiber stammt. Das ist ein Thema für Fortgeschrittene.

## 5. DuckDuckGo im Tor Browser

DuckDuckGo ist die **Standard-Suchmaschine** im Tor Browser. Standardmässig ist das aber die normale Webseite, nicht die .onion-Version. Mit der Option **"Onionize"** auf DuckDuckGo wechselst du zur .onion-Version.

## 6. Mini-Glossar

- **Clearnet:** Das normale, öffentliche Internet, erreichbar mit Standard-Browsern und Suchmaschinen.
- **Deep Web:** Alle Bereiche des Internets, die Suchmaschinen nicht erfassen, z. B. Online-Banking, E-Mail-Postfächer oder Firmen-Intranets. Das Deep Web ist **nicht** dasselbe wie das Darkweb.
- **Darkweb / Darknet:** Ein kleiner Teil des Internets, der nur mit spezieller Software wie Tor oder I2P erreichbar ist.
- **Onion-Routing:** Die Daten werden mehrfach verschlüsselt und über mehrere zufällige Server geleitet. Bei normalen Webseiten sind es drei (*Guard*, *Middle*, *Exit*). Bei .onion-Seiten verlässt die Verbindung das Tor-Netz gar nicht, darum gibt es dort keinen Exit-Server.
- **Letterboxing:** Graue Ränder im Tor Browser, die die echte Fenstergrösse vor Webseiten verbergen.
- **Bridge:** Ein Tor-Eingangsserver, dessen Adresse nicht öffentlich ist. Hilft, wenn Tor blockiert wird.
- **v3-Onion-Adresse:** Der aktuelle Standard. 56 Zeichen lang, endet auf `.onion`. Die alten, kurzen v2-Adressen funktionieren nicht mehr.

## Quellen

- [Tor Support: Schutz vor Browser-Fingerprinting](https://support.torproject.org/anti-fingerprinting/)
- [Tor Support: Letterboxing](https://support.torproject.org/glossary/letterboxing)
- [Tor Support: Tor Browser mit VPN](https://support.torproject.org/faq/faq-5/)
- [Tor Support: Wenn Tor blockiert ist](https://support.torproject.org/tor-browser/circumvention/unblocking-tor/)
- [Tor Browser Handbuch: Bridges](https://tb-manual.torproject.org/bridges)
- [Tor Support: DuckDuckGo als Standard-Suchmaschine](https://support.torproject.org/tbb/tbb-24/)
- [Tails](https://tails.net) · [Whonix](https://www.whonix.org)
