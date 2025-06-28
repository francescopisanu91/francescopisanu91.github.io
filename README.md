# Modèle de page web personnelle LIPN

## Cloner la page

Depuis la ligne de commande de votre ordinateur :

```bash
git clone https://depot.lipn.univ-paris13.fr/garciaflores/page_perso_lipn.git
```

## Adapter la page

1. Ouvrir le fichier index.html avec votre éditeur préféré
2. Adapter le contenu des éléments suivants :

- [ ] Nom
- [ ] Photo
- [ ] Mail
- [ ] Bureau
- [ ] Téléphone
- [ ] Thèmes de recherche
- [ ] Publications
- [ ] Enseignement
- [ ] Lien associé à la touche _more publications_
- [ ] Liens des icônes associées aux liens OrcID, DBLP et HAL

Voici d'autres exemples des pages LIPN faites avec ce thème :

- [Laure](https://lipn.univ-paris13.fr/~petrucci/)
- [Jorge](https://www-lipn.univ-paris13.fr/~garciaflores/)
- [Étienne](https://lipn.univ-paris13.fr/~andre/)

## Vérifier les modifications localement

Vous pouvez ouvrir localement la page pour vérifier vos modifications en ouvrant, avec le navigateur Firefox, en spécifiant l'adresse locale sur la bar d'adresse. *Essayez votre page avec plusieurs navigateurs, parce que Safari ou Chrome sont parfois plus tolérants à des balises Html non fermés et le rendu est différent que sur Firefox*. 

![Barre d'adresse URL du navigateur Firefox montrant comment charger la page localement sur l'adresse `file:///home/garciaflores/code/html/page_perso_lipn/public_html/index.html`](public_html/images/firefox.png)

## Déployer la page

1. Allez sur le répertoire local `page_perso_lipn/public_html` de votre ordinateur

```bash
$ cd /home/mon_repertoire/page_perso_lipn/public_html
```

2. Copiez le fichier `index.html` et les répertoires `assets` et `images` vers le dossier `public_html` associé à votre compte LIPN dans le disque partagé via la passerelle `lipnssh`. Voici comment procéder à partir de la ligne de commande.

Reemplacez `mon_utilisateur_lipn` par votre nom d'utilisateur

```bash
$ ls
assets  images  index.html

$ scp -r * mon_utilisateur_lipn@lipnssh.univ-paris13.fr:~/public_html
fontawesome-webfont.svg?v=4.7.0                                                                                                        100%  434KB  37.5MB/s   00:00
fontawesome-webfont.woff2?v=4.7.0                                                                                                      100%   75KB  28.1MB/s   00:00
fontawesome-webfont.eot?                                                                                                               100%  162KB  26.0MB/s   00:00
fontawesome-webfont.ttf?v=4.7.0                                                                                                        100%  162KB  26.8MB/s   00:00
fontawesome-webfont.woff?v=4.7.0                                                                                                       100%   96KB  23.4MB/s   00:00
fontawesome-webfont.eot?v=4.7.0                                                                                                        100%  162KB  38.1MB/s   00:00
util.js                                                                                                                                100%   12KB   6.3MB/s   00:00
skel.min.js                                                                                                                            100% 9085     7.2MB/s   00:00
jquery.min.js                                                                                                                          100%   94KB  32.9MB/s   00:00
main.js                                                                                                                                100% 6532     6.2MB/s   00:00
main.css                                                                                                                               100%   70KB  21.1MB/s   00:00
font-awesome.min.css                                                                                                                   100%   30KB  12.0MB/s   00:00
nathalie.jpg                                                                                                                           100%   34KB  19.2MB/s   00:00
firefox.png                                                                                                                            100%   16KB   8.9MB/s   00:00
index.html                                                                                                                             100%   11KB   6.3MB/s   00:00
```

## Vérifier la page sur le site web

Allez sur votre page perso pour vérifier que vos modifications sont bien sur le site LIPN :

https://lipn.univ-paris13.fr/~mon_user_lipn/

# En cas de panne
## Si vous n'arrivez pas à téléverser vos données par `scp`

Il se peut que vous vous êtes trompé de mot de passe et le système vous a bloquer. Il faut attendre 15 minutes, et commencer par essayer la commande suivante : (bien sur en remplaçant `pernelle` par votre nom d'utilisateur LIPN.
```bash
$ scp pernelle@lipnssh.univ-paris13.fr
```

### Si la page ne s'affiche pas correctement

Si quelque balise a été perdue pendant l'adaptation et le rendu de la page ne correspond pas à votre version locale, installez l'IDE [VSCodium](https://vscodium.com/) qui permet de mieux déboguer du HTML (surtout, comparez la section ou les balises principales s'ouvrent et se ferment). 

# Remerciements

Merci à Nathalie de nous avoir autorisé à utiliser ses données ;)
