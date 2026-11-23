# Tor Browser sur Linux

[← Retour à l'aperçu](../../README.fr.md)

Le Tor Browser fonctionne sur tous les systèmes Linux modernes. Il y a deux méthodes. La **variante A** est la plus simple pour débuter.

## Variante A : Tor Browser Launcher (recommandé)

Le Tor Browser Launcher télécharge le Tor Browser officiel depuis le Tor Project, vérifie sa signature et le maintient à jour.

### Avec Flatpak (version la plus récente)

Linux Mint intègre déjà Flatpak. Sur les autres systèmes, [configure d'abord Flatpak](https://flathub.org/setup).

```bash
flatpak install flathub org.torproject.torbrowser-launcher -y
flatpak run org.torproject.torbrowser-launcher
```

### Avec apt (Ubuntu, Debian, Linux Mint)

```bash
sudo apt update
sudo apt install torbrowser-launcher
torbrowser-launcher
```

La version apt peut être obsolète. Si elle ne fonctionne pas, utilise la version Flatpak.

Au premier démarrage, le launcher télécharge le Tor Browser. Ensuite, tu trouves **Tor Browser** dans le menu des applications.

## Variante B : manuellement depuis torproject.org

1. Ouvre [torproject.org/download](https://www.torproject.org/download/) et clique sur **Download for Linux**.
2. *(Recommandé)* Vérifie la signature : [Vérifier la signature](https://support.torproject.org/tbb/how-to-verify-signature/)
3. Décompresse l'archive dans le terminal :

    ```bash
    cd ~/Downloads
    tar -xf tor-browser-linux-*.tar.xz
    ```

4. Va dans le dossier et lance le navigateur :

    ```bash
    cd tor-browser
    ./start-tor-browser.desktop
    ```

5. S'il ne démarre pas, rends d'abord le fichier exécutable :

    ```bash
    chmod +x start-tor-browser.desktop
    ```

Il faudra peut-être adapter le nom du fichier dans la commande `tar` à la version téléchargée. Selon la langue du système, le dossier peut s'appeler `~/Téléchargements` au lieu de `~/Downloads`.

## Premier démarrage

1. Clique sur **Connect** dans la première fenêtre et attends que la connexion soit établie.
2. Ouvre [check.torproject.org](https://check.torproject.org). La page doit afficher **« Congratulations »**.

## Régler le niveau de sécurité

1. Clique sur l'**icône du bouclier** à côté de la barre d'adresse.
2. Clique sur **Settings**.
3. Clique sur **Change** et choisis **Safer** ou **Safest**.
4. Clique sur **Save and restart**.

## Encore plus de protection : Tails

[Tails](https://tails.net) est un système d'exploitation à part qui démarre depuis une clé USB. Tout passe par Tor, et tout est effacé à l'arrêt. Il te faut une clé USB d'au moins 8 Go.

## Sources

- [Manuel du Tor Browser : installation](https://tb-manual.torproject.org/installation)
- [torbrowser-launcher sur GitHub](https://github.com/micahflee/torbrowser-launcher)
- [Tails : comment fonctionne Tails](https://tails.net/about)
