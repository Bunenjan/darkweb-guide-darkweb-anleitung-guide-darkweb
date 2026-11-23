# Tor Browser auf Linux

[← Zurück zur Übersicht](../../README.de.md)

Der Tor Browser läuft auf allen modernen Linux-Systemen. Es gibt zwei Wege. Für Anfänger ist **Variante A** am einfachsten.

## Variante A: Tor Browser Launcher (empfohlen)

Der Tor Browser Launcher lädt den offiziellen Tor Browser vom Tor-Projekt herunter, prüft die Signatur und hält ihn aktuell.

### Mit Flatpak (aktuellste Version)

Linux Mint hat Flatpak bereits eingebaut. Bei anderen Systemen zuerst [Flatpak einrichten](https://flathub.org/setup).

```bash
flatpak install flathub org.torproject.torbrowser-launcher -y
flatpak run org.torproject.torbrowser-launcher
```

### Mit apt (Ubuntu, Debian, Linux Mint)

```bash
sudo apt update
sudo apt install torbrowser-launcher
torbrowser-launcher
```

Die apt-Version kann veraltet sein. Funktioniert sie nicht, nimm die Flatpak-Version.

Beim ersten Start lädt der Launcher den Tor Browser herunter. Danach findest du **Tor Browser** im Startmenü.

## Variante B: Manuell von torproject.org

1. Öffne [torproject.org/download](https://www.torproject.org/download/) und klicke auf **Download for Linux**.
2. *(Empfohlen)* Prüfe die Signatur: [Signatur prüfen](https://support.torproject.org/tbb/how-to-verify-signature/)
3. Entpacke das Archiv im Terminal:

    ```bash
    cd ~/Downloads
    tar -xf tor-browser-linux-*.tar.xz
    ```

4. Wechsle in den Ordner und starte den Browser:

    ```bash
    cd tor-browser
    ./start-tor-browser.desktop
    ```

5. Startet er nicht, die Datei zuerst ausführbar machen:

    ```bash
    chmod +x start-tor-browser.desktop
    ```

Den Dateinamen im `tar`-Befehl musst du allenfalls an die heruntergeladene Version anpassen.

## Erster Start

1. Klicke im ersten Fenster auf **Connect** und warte, bis die Verbindung steht.
2. Öffne [check.torproject.org](https://check.torproject.org). Dort muss **"Congratulations"** stehen.

## Sicherheitsstufe einstellen

1. Klicke auf das **Schild-Symbol** neben der Adresszeile.
2. Klicke auf **Settings**.
3. Klicke auf **Change** und wähle **Safer** oder **Safest**.
4. Klicke auf **Save and restart**.

## Noch mehr Schutz: Tails

[Tails](https://tails.net) ist ein eigenes Betriebssystem, das vom USB-Stick startet. Alles läuft über Tor, und beim Herunterfahren wird alles gelöscht. Du brauchst dafür einen USB-Stick mit mindestens 8 GB.

## Quellen

- [Tor Browser Handbuch: Installation](https://tb-manual.torproject.org/installation)
- [torbrowser-launcher auf GitHub](https://github.com/micahflee/torbrowser-launcher)
- [Tails: So funktioniert Tails](https://tails.net/about)
