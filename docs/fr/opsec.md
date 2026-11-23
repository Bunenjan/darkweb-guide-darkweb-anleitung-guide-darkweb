# Sécurité avancée, OpSec et conseils pratiques

[← Retour à l'aperçu](../../README.fr.md)

Le Tor Browser protège ta connexion. Mais le vrai anonymat dépend surtout de ton comportement. Tu trouveras ici les erreurs typiques des débutants, des fonctions importantes comme les ponts Tor (bridges) et la différence avec des systèmes d'exploitation spécialisés.

## 1. Éviter les pièges OpSec typiques

- **Ne pas changer la taille de la fenêtre :** Le Tor Browser démarre volontairement avec une taille de fenêtre standard. Les sites web peuvent reconnaître ton appareil grâce à la taille de la fenêtre ou de l'écran (*empreinte du navigateur*, ou *fingerprinting*). Le Tor Browser s'en protège avec le **letterboxing** : il ajoute des marges grises et cache ainsi la vraie taille de la fenêtre. La taille standard reste quand même la plus sûre. Donc ne pas agrandir la fenêtre et ne pas naviguer en plein écran.
- **Pas de VPN en plus de Tor :** Le Tor Project le déconseille en général, sauf pour les utilisateurs avancés qui savent exactement comment configurer les deux correctement. Un fournisseur VPN connaît ta vraie adresse IP et en général tes données de paiement. Tu déplaces donc simplement ta confiance vers une entreprise. Si tu veux cacher que tu utilises Tor, utilise plutôt les **ponts Tor** (section 3).
- **Attention aux métadonnées des fichiers :** Les photos contiennent souvent des données EXIF comme le modèle d'appareil ou les coordonnées GPS ; les documents contiennent souvent l'auteur et l'heure de modification. Le plus sûr : ne partager aucun fichier personnel. Sinon, supprime d'abord les métadonnées, par exemple avec le programme *MAT2*.
- **Ne pas reprendre ses habitudes :** N'utilise jamais dans le Tor Browser le même pseudo, le même modèle de mot de passe ou la même photo de profil que sur l'Internet normal (clearnet).

## 2. Tor Browser, Tails ou Whonix ?

| Solution | Fonctionnement | Quand est-ce utile ? |
| --- | --- | --- |
| **Tor Browser** | Une appli normale sur Windows, macOS, Linux ou Android. | Pour naviguer en privé et faire des recherches. Peut laisser des traces sur le système principal, et un logiciel malveillant sur l'appareil met aussi le navigateur en danger. |
| **Tails** | Un système d'exploitation à part qui démarre depuis une clé USB et oublie tout à l'arrêt (*amnésique*). | Si ton ordinateur n'est pas entièrement fiable ou si aucune trace ne doit rester sur le disque dur. |
| **Whonix** | Deux machines virtuelles (Gateway et Workstation) qui font obligatoirement passer tout le trafic réseau par Tor. | Pour les utilisateurs avancés qui veulent une protection maximale contre les fuites d'IP dues à un logiciel malveillant ou à une erreur de programme. |

## 3. Contourner les blocages avec les ponts Tor

Certains fournisseurs d'accès, réseaux Wi-Fi publics (p. ex. dans les hôtels, les écoles ou les trains) ou pays bloquent les connexions au réseau Tor. Les **ponts** (bridges) aident dans ce cas : ce sont des serveurs d'entrée Tor dont les adresses ne sont pas publiques.

1. Ouvre **Settings** dans le Tor Browser et choisis **Connection** à gauche.
2. Descends jusqu'à la section **Bridges**.
3. Clique sur **Select a Built-In Bridge** et choisis un type :
    - **obfs4 :** déguise le trafic Tor en flux de données aléatoire.
    - **Snowflake :** fait passer ta connexion par des proxys gérés par des bénévoles. Utile en cas de blocages stricts.
4. Confirme avec **OK**. Le réglage est enregistré dès que tu fermes l'onglet.

Au tout premier démarrage, tu peux aussi passer par **Configure Connection** dans la fenêtre de démarrage.

## 4. Reconnaître les vrais sites

Sur le dark web, il n'y a pas d'autorités de certification comme sur le web normal. Les sites d'arnaque copient des services connus avec des adresses .onion légèrement modifiées.

- **Uniquement des sources officielles :** Ne reprends jamais d'adresses .onion depuis les réseaux sociaux, des forums ou des wikis non modérés. Passe toujours par le site normal du fournisseur, p. ex. via le bouton « .onion available », ou utilise la liste [Real-World Onion Sites](https://github.com/alecmuffett/real-world-onion-sites).
- **Signatures PGP :** Certains fournisseurs publient aussi leur adresse .onion ou des messages importants avec une **signature PGP** (*Pretty Good Privacy*). Avec des programmes comme *GnuPG* ou *Kleopatra*, tu peux vérifier si un message vient vraiment du véritable exploitant. C'est un sujet pour utilisateurs avancés.

## 5. DuckDuckGo dans le Tor Browser

DuckDuckGo est le **moteur de recherche par défaut** du Tor Browser. Par défaut, c'est toutefois le site normal et non la version .onion. Avec l'option **« Onionize »** sur DuckDuckGo, tu passes à la version .onion.

## 6. Mini-glossaire

- **Clearnet :** L'Internet normal et public, accessible avec des navigateurs et moteurs de recherche standard.
- **Deep web :** Toutes les parties d'Internet que les moteurs de recherche n'indexent pas, p. ex. la banque en ligne, les boîtes e-mail ou les intranets d'entreprise. Le deep web n'est **pas** la même chose que le dark web.
- **Dark web / darknet :** Une petite partie d'Internet accessible uniquement avec un logiciel spécial comme Tor ou I2P.
- **Routage en oignon (onion routing) :** Les données sont chiffrées plusieurs fois et passent par plusieurs serveurs choisis au hasard. Pour les sites normaux, il y en a trois (*guard*, *middle*, *exit*). Pour les sites .onion, la connexion ne quitte jamais le réseau Tor, il n'y a donc pas de serveur de sortie.
- **Letterboxing :** Des marges grises dans le Tor Browser qui cachent la vraie taille de ta fenêtre aux sites web.
- **Pont (bridge) :** Un serveur d'entrée Tor dont l'adresse n'est pas publique. Utile quand Tor est bloqué.
- **Adresse onion v3 :** Le standard actuel. 56 caractères, se termine par `.onion`. Les anciennes adresses v2, plus courtes, ne fonctionnent plus.

## Sources

- [Support Tor : protection contre l'empreinte du navigateur](https://support.torproject.org/anti-fingerprinting/)
- [Support Tor : letterboxing](https://support.torproject.org/glossary/letterboxing)
- [Support Tor : utiliser le Tor Browser avec un VPN](https://support.torproject.org/faq/faq-5/)
- [Support Tor : que faire si Tor est bloqué](https://support.torproject.org/tor-browser/circumvention/unblocking-tor/)
- [Manuel du Tor Browser : ponts](https://tb-manual.torproject.org/bridges)
- [Support Tor : DuckDuckGo moteur de recherche par défaut](https://support.torproject.org/tbb/tbb-24/)
- [Tails](https://tails.net) · [Whonix](https://www.whonix.org)
