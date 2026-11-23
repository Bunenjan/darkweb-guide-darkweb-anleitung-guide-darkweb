# Accéder au dark web – en sécurité, étape par étape

Langue : [English](README.md) · [Deutsch](README.de.md) · **Français**

Un guide simple pour accéder au dark web en toute sécurité : d'abord installer le Tor Browser sur ton appareil, puis visiter tes premiers sites .onion. Pour Windows, macOS, Linux, Android (p. ex. Samsung) et iPhone.

## Comment procéder

1. **Installer le Tor Browser :** choisis ton appareil ci-dessous.
2. **Régler le niveau de sécurité :** expliqué dans chaque guide.
3. **Accéder au dark web :** [Premiers pas sur le dark web](docs/fr/darkweb.md)
4. **Aller plus loin :** [Sécurité avancée, OpSec et conseils pratiques](docs/fr/opsec.md)

## Qu'est-ce que le dark web ?

Le dark web est la partie d'Internet qu'on ne peut atteindre qu'avec un logiciel spécial comme Tor. Les adresses s'y terminent par `.onion`. Un navigateur normal comme Chrome ou Safari ne peut pas les ouvrir.

Sur le dark web, il y a des sites tout à fait normaux (journaux, moteurs de recherche, services de messagerie), mais aussi beaucoup d'arnaques et de contenus illégaux. C'est pourquoi il est important de respecter les règles de ce guide.

## Qu'est-ce que Tor ?

Le Tor Browser fait passer ta connexion par plusieurs serveurs du réseau Tor. Les sites web ne voient pas d'où tu viens, et ton fournisseur d'accès ne voit pas quels sites tu visites.

Utiliser Tor est légal en Suisse et dans la plupart des autres pays. Ce qui est punissable, c'est ce qu'on en fait, exactement comme sur l'Internet normal.

> Ceci est un guide non officiel. Les pages officielles du Tor Project font toujours foi : [torproject.org](https://www.torproject.org) et le [manuel du Tor Browser](https://tb-manual.torproject.org).
>
> L'interface du Tor Browser est peut-être en français sur ton appareil. Les noms des boutons sont indiqués ici en anglais, comme dans la version d'origine.

## Étape 1 : installer le Tor Browser

| Appareil | App | Guide |
| --- | --- | --- |
| Windows 10 / 11 | Tor Browser | [windows.md](docs/fr/windows.md) |
| macOS 10.15 et plus récent | Tor Browser | [mac.md](docs/fr/mac.md) |
| Linux (p. ex. Ubuntu, Linux Mint) | Tor Browser | [linux.md](docs/fr/linux.md) |
| Android (p. ex. Samsung) | Tor Browser pour Android | [android.md](docs/fr/android.md) |
| iPhone / iPad | Onion Browser | [iphone.md](docs/fr/iphone.md) |

## La règle la plus importante : uniquement des sources officielles

Il existe beaucoup de fausses applis et de faux téléchargements « Tor » contenant des logiciels malveillants ou de la publicité. Télécharge uniquement depuis ces endroits :

- **Windows, macOS, Linux :** [torproject.org/download](https://www.torproject.org/download/)
- **Android :** Google Play Store, F-Droid (Guardian Project) ou le site du Tor Project
- **iPhone :** « Onion Browser » dans l'App Store (recommandé par le Tor Project)

## Étape 2 : régler le niveau de sécurité

Le Tor Browser a trois niveaux de sécurité. Par défaut, il est réglé sur **Standard**.

| Niveau | Ce qui se passe |
| --- | --- |
| Standard | Toutes les fonctions sont activées. |
| Safer | Les fonctions dangereuses sont désactivées. JavaScript est désactivé sur les sites sans HTTPS. L'audio et la vidéo démarrent seulement sur clic. |
| Safest | JavaScript est désactivé partout. Certaines images et polices sont désactivées. Seuls les sites simples fonctionnent. |

Pour débuter, **Safer** ou **Safest** est recommandé. Chaque guide explique comment changer le niveau.

## Règles de comportement

Le plus grand danger n'est pas la technique, mais ton propre comportement.

- **Ne rien télécharger et n'ouvrir aucun fichier.** Les PDF et les fichiers Office peuvent établir une connexion en dehors de Tor ou contenir des logiciels malveillants.
- **Ne jamais saisir de vraies données :** pas de nom, pas d'adresse e-mail, pas de mots de passe.
- **N'installer aucun module complémentaire ni extension.**
- **Ne rien acheter.** Beaucoup de boutiques du dark web sont des arnaques, et une grande partie de ce qui s'y vend est illégale.
- **Ne pas cliquer sur des liens de listes inconnues** (TikTok, Discord, « listes de liens du dark web »).
- **Pas sur un appareil professionnel ou scolaire** ni sur un réseau d'entreprise. Cela enfreint généralement les directives informatiques.
- **Installer les mises à jour immédiatement** quand le navigateur le demande.

## Tester si Tor fonctionne

Ouvre [check.torproject.org](https://check.torproject.org) dans le Tor Browser. Si la page affiche **« Congratulations »**, ta connexion passe par Tor.

## Étape 3 : accéder au dark web

Comment ouvrir ton premier site .onion et où trouver des adresses sûres : **[Premiers pas sur le dark web](docs/fr/darkweb.md)**

## Étape 4 : aller plus loin

Erreurs OpSec typiques, ponts Tor contre les blocages, Tor Browser vs Tails vs Whonix et un mini-glossaire : **[Sécurité avancée, OpSec et conseils pratiques](docs/fr/opsec.md)**

## Sources

- [Manuel du Tor Browser : installation](https://tb-manual.torproject.org/installation)
- [Support Tor : installation et configuration requise](https://support.torproject.org/tbb/tbb-11/)
- [Manuel du Tor Browser : paramètres de sécurité](https://tb-manual.torproject.org/security-settings)
- [Manuel du Tor Browser : Android](https://tb-manual.torproject.org/mobile-tor)
- [Support Tor : Tor sur iOS](https://support.torproject.org/tormobile/tormobile-3/)
- [EFF Surveillance Self-Defense : Tor sur Android et iPhone](https://ssd.eff.org/module/tor)

État : novembre 2026
