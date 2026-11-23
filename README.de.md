# Ins Darkweb – sicher und Schritt für Schritt

Sprache: [English](README.md) · **Deutsch** · [Français](README.fr.md)

Eine einfache Anleitung, wie du sicher ins Darkweb kommst: zuerst den Tor Browser auf deinem Gerät installieren, dann die ersten .onion-Seiten besuchen. Für Windows, macOS, Linux, Android (z. B. Samsung) und iPhone.

## So gehst du vor

1. **Tor Browser installieren:** Wähle unten dein Gerät.
2. **Sicherheitsstufe einstellen:** steht in jeder Anleitung.
3. **Ins Darkweb gehen:** [Erste Schritte im Darkweb](docs/de/darkweb.md)
4. **Weiterführend:** [Sicherheit, OpSec und Praxis-Tipps](docs/de/opsec.md)

## Was ist das Darkweb?

Das Darkweb ist der Teil des Internets, den man nur mit einer speziellen Software wie Tor erreicht. Die Adressen dort enden auf `.onion`. Ein normaler Browser wie Chrome oder Safari kann sie nicht öffnen.

Im Darkweb gibt es ganz normale Seiten (Zeitungen, Suchmaschinen, E-Mail-Dienste), aber auch viel Betrug und illegale Inhalte. Darum ist es wichtig, sich an die Regeln in dieser Anleitung zu halten.

> Dies ist eine inoffizielle Anleitung. Massgebend sind immer die offiziellen Seiten des Tor-Projekts: [torproject.org](https://www.torproject.org) und das [Tor Browser Handbuch](https://tb-manual.torproject.org).

## Was ist Tor?

Der Tor Browser leitet deine Verbindung über mehrere Server im Tor-Netzwerk. So sieht eine Webseite nicht, von wo du kommst, und dein Internetanbieter sieht nicht, welche Seiten du besuchst. Mit dem Tor Browser kannst du auch Seiten öffnen, deren Adresse auf `.onion` endet.

Tor zu benutzen ist in der Schweiz und den meisten anderen Ländern legal. Strafbar ist, was man damit tut, genau wie im normalen Internet.

## Schritt 1: Tor Browser installieren

| Gerät | App | Anleitung |
| --- | --- | --- |
| Windows 10 / 11 | Tor Browser | [windows.md](docs/de/windows.md) |
| macOS 10.15 und neuer | Tor Browser | [mac.md](docs/de/mac.md) |
| Linux (z. B. Ubuntu, Linux Mint) | Tor Browser | [linux.md](docs/de/linux.md) |
| Android (z. B. Samsung) | Tor Browser für Android | [android.md](docs/de/android.md) |
| iPhone / iPad | Onion Browser | [iphone.md](docs/de/iphone.md) |

## Die wichtigste Regel: nur aus offiziellen Quellen

Es gibt viele gefälschte "Tor"-Apps und Downloads mit Schadsoftware oder Werbung. Lade nur von diesen Orten:

- **Windows, macOS, Linux:** [torproject.org/download](https://www.torproject.org/download/)
- **Android:** Google Play Store, F-Droid (Guardian Project) oder die Tor-Projekt-Webseite
- **iPhone:** "Onion Browser" im App Store (vom Tor-Projekt empfohlen)

## Schritt 2: Sicherheitsstufe einstellen

Der Tor Browser hat drei Sicherheitsstufen. Standardmässig steht er auf **Standard**.

| Stufe | Was passiert |
| --- | --- |
| Standard | Alle Funktionen sind aktiv. |
| Safer | Gefährliche Funktionen sind aus. JavaScript ist auf Seiten ohne HTTPS aus. Audio und Video starten erst auf Klick. |
| Safest | JavaScript ist überall aus. Einige Bilder und Schriften sind aus. Nur einfache Seiten funktionieren. |

Für den Einstieg empfiehlt sich **Safer** oder **Safest**. Wie man die Stufe ändert, steht in jeder Anleitung.

## Verhaltensregeln

Die grösste Gefahr ist nicht die Technik, sondern das eigene Verhalten.

- **Nichts herunterladen und keine Dateien öffnen.** PDFs und Office-Dateien können eine Verbindung ausserhalb von Tor aufbauen oder Schadsoftware enthalten.
- **Keine echten Daten eingeben:** kein Name, keine E-Mail-Adresse, keine Passwörter.
- **Keine Add-ons oder Erweiterungen installieren.**
- **Nichts kaufen.** Viele Shops im Darkweb sind Betrug, vieles ist illegal.
- **Keine Links aus unbekannten Listen** (TikTok, Discord, "Darkweb-Linklisten") anklicken.
- **Nicht auf Firmen- oder Schulgeräten** und nicht im Firmennetz. Das verstösst meist gegen die IT-Richtlinien.
- **Updates sofort installieren**, wenn der Browser danach fragt.

## Testen, ob Tor funktioniert

Öffne im Tor Browser [check.torproject.org](https://check.torproject.org). Wenn dort **"Congratulations"** steht, läuft deine Verbindung über Tor.

## Schritt 3: Ins Darkweb gehen

Wie du deine erste .onion-Seite öffnest und wo du sichere Adressen findest, steht hier: **[Erste Schritte im Darkweb](docs/de/darkweb.md)**

## Schritt 4: Weiterführend

Typische OpSec-Fehler, Tor Bridges gegen Blockaden, Tor Browser vs. Tails vs. Whonix und ein Mini-Glossar: **[Sicherheit, OpSec und Praxis-Tipps](docs/de/opsec.md)**

## Quellen

- [Tor Browser Handbuch: Installation](https://tb-manual.torproject.org/installation)
- [Tor Support: Installation und Systemanforderungen](https://support.torproject.org/tbb/tbb-11/)
- [Tor Browser Handbuch: Sicherheitseinstellungen](https://tb-manual.torproject.org/security-settings)
- [Tor Browser Handbuch: Android](https://tb-manual.torproject.org/mobile-tor)
- [Tor Support: Tor auf iOS](https://support.torproject.org/tormobile/tormobile-3/)
- [EFF Surveillance Self-Defense: Tor auf Android und iPhone](https://ssd.eff.org/module/tor)

Stand: November 2026
