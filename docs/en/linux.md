# Tor Browser on Linux

[← Back to overview](../../README.md)

Tor Browser runs on all modern Linux systems. There are two ways. **Option A** is the easiest for beginners.

## Option A: Tor Browser Launcher (recommended)

Tor Browser Launcher downloads the official Tor Browser from the Tor Project, verifies its signature and keeps it up to date.

### With Flatpak (latest version)

Linux Mint has Flatpak built in. On other systems, [set up Flatpak](https://flathub.org/setup) first.

```bash
flatpak install flathub org.torproject.torbrowser-launcher -y
flatpak run org.torproject.torbrowser-launcher
```

### With apt (Ubuntu, Debian, Linux Mint)

```bash
sudo apt update
sudo apt install torbrowser-launcher
torbrowser-launcher
```

The apt version may be outdated. If it does not work, use the Flatpak version.

On first start, the launcher downloads Tor Browser. After that, you will find **Tor Browser** in the application menu.

## Option B: Manually from torproject.org

1. Open [torproject.org/download](https://www.torproject.org/download/) and click **Download for Linux**.
2. *(Recommended)* Verify the signature: [Verify the signature](https://support.torproject.org/tbb/how-to-verify-signature/)
3. Extract the archive in the terminal:

    ```bash
    cd ~/Downloads
    tar -xf tor-browser-linux-*.tar.xz
    ```

4. Go into the folder and start the browser:

    ```bash
    cd tor-browser
    ./start-tor-browser.desktop
    ```

5. If it does not start, make the file executable first:

    ```bash
    chmod +x start-tor-browser.desktop
    ```

You may need to adjust the file name in the `tar` command to match the version you downloaded.

## First start

1. Click **Connect** in the first window and wait until the connection is established.
2. Open [check.torproject.org](https://check.torproject.org). It must say **"Congratulations"**.

## Set the security level

1. Click the **shield icon** next to the address bar.
2. Click **Settings**.
3. Click **Change** and choose **Safer** or **Safest**.
4. Click **Save and restart**.

## Even more protection: Tails

[Tails](https://tails.net) is a separate operating system that starts from a USB stick. Everything runs through Tor, and everything is erased when you shut down. You need a USB stick with at least 8 GB.

## Sources

- [Tor Browser Manual: Installation](https://tb-manual.torproject.org/installation)
- [torbrowser-launcher on GitHub](https://github.com/micahflee/torbrowser-launcher)
- [Tails: How Tails works](https://tails.net/about)
