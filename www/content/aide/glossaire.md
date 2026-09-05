+++
title = "Glossaire"
+++

<style>
  dt + dd:has(+ dd), dd + dd { display: list-item; list-style-type: "-  "; }
  dd p { margin: 0.7em 0; }
  code { font-family: monospace; }
  .footnotes { font-size: smaller; }
  .footnotes li p { margin: 0.2em 0; }
</style>


Analyse et optimisation
--------------------------------------------------------------------------------

### Bigrammes

[Bigramme]{#bigramme}

: Enchainement de deux touches.

[SFB <i lang="en">(same-finger bigram)</i>]{#sfb}

: Aussi appelé « bigramme de même doigt » : enchainement de deux touches
différentes avec le même doigt. C’est une source d’inconfort ou d’erreurs, notamment
à haute vitesse.

[SFU <i lang="en">(same-finger usage)</i>]{#sfu}

: Taux de SFB relevés dans un corpus de texte, exprimé en % du nombre total de
bigrammes. Plus le taux est bas, mieux c’est.

[SKB <i lang="en">(same-key bigram)</i>]{#skb}

: Répétition de la même touche, par exemple pour produire `nn` avec n’importe
quelle disposition de clavier, ou `és` en Ergo‑L.

[SKU <i lang="en">(same-key usage)</i>]{#sku}

: Taux de SKB relevés dans un corpus de texte, exprimé en % du nombre total de
bigrammes. Théoriquement, il ne dépend que du corpus ; mais il peut augmenter
avec l’usage de touches mortes.

[SHB <i lang="en">(same-hand bigram)</i>]{#shb}

: Aussi appelé « bigramme de même main » : enchainement de deux touches sous
deux doigts différents de la même main. C’est ce que cherche à éviter Dvorak,
qui privilégie les alternances de mains pour des raisons historiques, liées aux
contraintes des machines à écrire mécaniques de l’époque.

[SHU <i lang="en">(same-hand usage)</i>]{#shu}

: Taux de SHB relevés dans un corpus de texte, exprimé en % du nombre total de
bigrammes. Plus le taux est bas, plus la disposition favorise l’alternance de
mains ; plus le taux est élevé, plus la disposition favorise les roulements.

[Extension]{#extension}

: Mouvement pour atteindre une touche qui est soit sur une autre colonne que la
position de repos, soit à une distance supérieure à une touche.

[LSB <i lang="en">(lateral stretch bigram)</i>]{#lsb}

: Bigramme de même main comportant une extension, par exemple [L]{.kbd}[H]{.kbd}
en Azerty ou Qwerty.

[Ciseau]{#ciseau}

: Bigramme nécessitant un changement de rangée inconfortable, par exemple
[C]{.kbd}[R]{.kbd} en Azerty ou Qwerty. Le terme « ciseau » est utilisé ici
au singulier comme substantif de « mouvement en ciseaux », comme on le fait dans
divers sports.

[Roulement intérieur]{#roulement}

: Deux touches ou plus enchainées sur une même main, dans le sens de
l’auriculaire vers l’index. C’est l’enchainement considéré comme le plus
confortable qui soit.

Roulement extérieur

: Deux touches ou plus enchainées sur une même main, dans le sens de l’index
vers l’auriculaire.

### Trigrammes

[Trigramme]{#trigramme}

: Enchainement de trois touches.

[SFS <i lang="en">(same-finger skipgram)</i>]{#sfs}

: Un SFB avec une touche d’un autre doigt intercalée au milieu, par exemple
[E]{.kbd}[A]{.kbd}[D]{.kbd} ou [B]{.kbd}[U]{.kbd}[T]{.kbd} en Azerty ou Qwerty.

[SKS <i lang="en">(same-key skipgram)</i>]{#sks}

: Un SKB avec une touche d’un autre doigt intercalée au milieu, par exemple
[E]{.kbd}[R]{.kbd}[E]{.kbd} ou [E]{.kbd}[L]{.kbd}[E]{.kbd} en Azerty ou Qwerty.

[Redirection]{#redirection}

: Trois touches enchainées sur une même main avec un changement de direction,
e.g. [D]{.kbd}[S]{.kbd}[F]{.kbd} ou [K]{.kbd}[J]{.kbd}[L]{.kbd} en Azerty ou
Qwerty.

Mauvaise redirection

: Une redirection où l’index n’intervient pas. L’un des pires enchainements
faisables sur un clavier, sinon le pire.


Support logiciel
--------------------------------------------------------------------------------
<!-- Nota : la distinction keycode/scancode échappe à beaucoup de personnes, y
compris à des développeurs qui travaillent sur la question — comme ça a été le
cas au sein de la talentueuse équipe de KMonad sur ce ticket Github :
https://github.com/kmonad/kmonad/issues/111 -->

[Scan code]{#scan-code-def}

: Données envoyées par un clavier physique à un ordinateur lorsqu’on appuie
ou relâche une touche. Par suite aux évolutions technologiques (PS/2, USB, etc.),
il existe plusieurs ensembles de scan codes.

: Souvent associé au seul code envoyé lors de la _pression_ d’une touche, en
particulier avec les scan codes « XT » ou « ensemble 1 ». Il permet alors
d’identifier la touche qui a été pressée dans un périphérique de saisie, au plus
bas niveau de l’OS.

[Key code]{#key-code-def}

: Code identifiant une touche sur un clavier. Ce code est propre à chaque
système d’exploitation. Ce dernier se charge de convertir les différentes
conventions de _scan code_ en _key code_, permettant ainsi de faire abstraction
de la technologie du clavier pour développer des dispositions de clavier.

[Point de code]{#point-de-code-def} (<i lan="en">code point</i>)

: 🚧 définition à rajouter 🚧 (cf. [point de code] sur Wikipedia).

[Modificateur]{#modificateur-def}

: 🚧 définition à rajouter 🚧 (Modificateurs courants : `Shift`, `Caps`,
`AltGr`, etc.).

[Couche]{#couche-def} (<i lang="en">layer</i>)

: Abstraction pour pouvoir disposer plusieurs caractères sur une même touche.

    Exemple le plus courant de couches : en tapant des lettres sur la couche
    *alpha* on obtient les lettres en minuscules, en gardant la touche
    [Shift]{.kbd} enfoncée on obtient les lettres en majuscules, ce sont donc
    deux couches différentes.

    Ce concept de couches permet de diminuer le nombre de touches nécessaires sur
    un clavier et brille particulièrement sur les petits claviers ergonomiques
    en diminuant la distance que les doigts ont à parcourir.

    Notez qu’une [touche morte] peut également être considérée comme définissant
    une couche, au même titre qu’un [modificateur].

    <!-- TODO: liens vers les couches typo et symboles -->

[Touche morte]{#touche-morte-def} (<i lang="en">dead key</i>)

: Touche de clavier qui ne produit aucun résultat lorsqu’elle est enfoncée puis
relâchée, mais modifie le comportement de la prochaine touche qui sera enfoncée.
Une touche morte est généralement utilisée pour produire des lettres accentuées
ou autres [diacritiques].

    Exemple : la touche [\^]{.kbd} sur le clavier Azerty puis [E]{.kbd} donne la
    lettre `ê`.

[Diacritique]{#diacritique-def}

: Signe accompagnant une lettre ou un graphème pour en modifier le sens ou la
prononciation.

    Exemple : la cédille pour « ç » ou les accents sur les voyelles. Plus de
    détails dans l’article [Wikipedia][diacritiques-wiki].

[modificateur]:      #modificateur-def
[point de code]:     https://fr.wikipedia.org/wiki/Point_de_code
[touche morte]:      #touche-morte-def
[diacritiques-wiki]: https://fr.wikipedia.org/wiki/Diacritique
[diacritiques]:      #diacritique-def

### Windows

AHK

: Abréviation du logiciel [AutoHotKey] qui permet de manière globale de créer
des scripts pour Windows. Dans le cas des dispositions clavier, il est utilisé
pour modifier les touches envoyées par le clavier et ainsi créer un pilote de
disposition ne necessitant pas d’installation.

[KbdEdit]

: Logiciel qui permet de créer des pilotes Windows pour des dispositions clavier
personnalisées. Il est beaucoup plus complet que MSKLC (voir ci-dessous).
Contrairement à ce dernier, il est payant et n’est pas officiellement supporté
par Microsoft.

KLC

: Fichier avec extension `.klc` décrivant une disposition clavier pour Microsoft
Keyboard Layout Creator (MSKLC).

    C’est un fichier source pour créer les pilotes Windows.

MSKLC

: Abréviation du logiciel [Microsoft Keyboard Layout Creator] qui permet de
créer des pilotes Windows pour des dispositions clavier personnalisées.

    Il peut être utilisé de manière autonome ou par l’intermédiaire de [Kalamine],
    ce dernier corrigeant ainsi de nombreuses limitations de MSKLC.

Virtual Key (VK, touche virtuelle)

: Code de touche spécifique à Windows, de plus haut niveau que le key code.
Il est utilisé pour définir le placement des touches spéciales ainsi que le
comportement d’une touche lorsqu’elle est utilisée dans un raccourci clavier.

[AutoHotKey]: https://www.autohotkey.com/
[Kalamine]: https://github.com/OneDeadKey/kalamine?tab=readme-ov-file#wkalamine
[KbdEdit]: http://www.kbdedit.com/
[Microsoft Keyboard Layout Creator]: https://www.microsoft.com/en-us/download/details.aspx?id=102134


### macOS

keylayout

: 🚧 définition à rajouter 🚧

Karabiner

: 🚧 définition à rajouter 🚧


### Linux

#### Explication simplifée du processus : appui sur une touche → production de caractère

1. Le clavier produit un [scan code].
2. L’<abbr title="Operating System">OS</abbr> transforme le [scan code] en [keycode].
3. Le [keycode] est transformé en [keysym] selon le [groupe] les
   [modificateurs] actifs, ces derniers déterminant la [couche] active.
4. La [keysym] est transformée en caractère(s) par la méthode de saisie
   ([Compose] par défaut) si active, sinon en utilisant la table de
   conversion standard de XKB.

[scan code]: #scan-code-def
[keycode]: #keycode-xkb-def
[Compose]: #compose-def
[modificateurs]: #modificateur-def
[couche]: #couche-def
[groupe]: #group-xkb-def


#### Environnement

[X11]

: X est un protocole de système de fenêtrage. [X11] en est la onzième version
majeure.

[X.Org]

: Le principal [serveur X][X11] utilisé sur Linux.

Wayland

: Un protocole de système de fenêtrage, destiné à remplacer X11 qui n’est plus
maintenu. Bien qu’en développement depuis 2008, son implémentation dans les
environnements de bureau majeurs n’a commencé à être suffisante que dans les
années 2020.

XKB (_X_ <em>K</em>eyboard <em>E</em>xtension)

: Un __[protocole][XKB protocol]__ défini comme extension de X11 et dédié à la gestion des
claviers.

: C’est aussi utilisé pour le [__format__ texte de configuration][XKB text format]
des dispositions clavier.

: Par abus de langage c'est aussi la __base de données__ des configurations clavier,
[`xkeyboard-config`][xkeyboard-config].

[Compose]{#compose-def}

: Une __méthode de saisie__ (<i lang="en">input method</i> ou IM). C’est notamment
ce qui permet aux touches mortes système (autres que `1dk`) de fonctionner.
Elle porte ce nom car elle _compose_ – entendre : combine – plusieurs [keysyms]
en un[^composed-keysym] nouveau keysym.

    <!-- XXX le diacritique combinant est mal supporté avec certaines polices,
    dont DejaVu Sans Mono : `◌́e` est affiché « é » et non «  ◌́e` ». -->
    Exemples : la séquence `◌́e` est transformée en `é`, `n~` en `ñ`, `+-` en `±`
    et `<3` en `♥`.

: Une __[touche][touche Compose]__ qui active la _méthode de saisie_ Compose pour
les touches pressées à la suite. Cette touche n’est pas présente sur les claviers
physiques modernes, mais elle est peut être configurée dans l’OS avec les options
de clavier.

: La __[keysym]__ `<Multi_key>`, qui est placée sur la _touche_ Compose.

XCompose

: Une __[spécification][XCompose]__ de Compose pour les systèmes basés sur X11 et
Wayland. Il existe plusieurs implémentations: `XIM` (référence), `xkbcommon`,
`Gtk`, `Qt`, `ibus`, etc. Notez qu’il existe des différences entre ces
implémentations.

: Un __format__ pour configuer la méthode de saisie XCompose.

: Les __fichiers__ de configuration correspondants. En particulier :

    - `/usr/share/X11/locale/**/Compose` : les fichiers système, organisés par
      locale.
    - `~/.XCompose` : le fichier utilisateur par défaut.

[X11]:              https://fr.wikipedia.org/wiki/X_Window_System
[X.Org]:            https://fr.wikipedia.org/wiki/X.Org
[Wayland]:          https://fr.wikipedia.org/wiki/Wayland
[XKB protocol]:     https://www.x.org/releases/current/doc/kbproto/xkbproto.html
[XKB text format]:  https://xkbcommon.org/doc/current/keymap-text-format-v1.html
[xkeyboard-config]: https://gitlab.freedesktop.org/xkeyboard-config/xkeyboard-config
[touche Compose]:   https://fr.wikipedia.org/wiki/Touche_de_composition
[XCompose]:         https://linux.die.net/man/3/xcompose

[keysym]:           #keysym-def
[keysyms]:          #keysym-def
[points de code]:   #point-de-code-def

<!-- notes de bas de page -->
[^composed-keysym]: Le cas le plus fréquent est _un_ keysym, mais il est
    possible d’en produire plusieurs. C’est indispensable pour certains
    caractères qui nécessitent plusieurs [points de code], comme « ė̄ » (`U+0117
    + U+0304`), mais aussi
    👩🏿‍🚀👩🏾‍🚀👩🏽‍🚀👩🏼‍🚀👩🏻‍🚀👩‍🚀, qui
    requiert au moins deux [points de code] pour chaque emoji.


#### XKB

[Keycode]{#keycode-xkb-def}

: Code identifiant une touche physique sur un clavier. Le code _brut_ (raw
keycode) est le code numérique issu du traitement bas niveau par le noyau, alors
que le code _symbolique_ est le nom donné dans les fichiers XKB pour faciliter
la configuration haut-niveau du clavier. On distinguera le code brut du _noyau_
de celui de XKB, ce dernier étant obtenu en ajoutant 8 au premier.

    Exemple : sur un clavier QWERTY, le code brut noyau de la touche `Q` est
    `16`[^code-brut-noyau], le code brut sur XKB est `16 + 8 = 24` et son code
    symbolique est `AD01`[^code-symbolique-iso-9995].

    Noter qu’un clavier QWERTY et un clavier AZERTY produisent habituellement
    des keycodes identiques pour les touches situées au même emplacement : ainsi
    la touche imprimée `Q` sur le clavier QWERTY produira le même keycode que la
    touche imprimée `A` sur un clavier imprimé AZERTY. En effet, c’est la
    configuration du clavier dans XKB et non le clavier lui-même qui définit la
    correspondance touche / [keysym].

[Keysym]{#keysym-def}

: Code numérique identifiant un symbole sur le _capuchon_ d’une touche. Ce mot
vient de l’anglais « <i lang="en">key symbol</i> ». Les keysyms sont également
associées à des noms anglais pour faciliter leur utilisation. Exemples : `a`,
`agrave` pour « à », `Shift_L` pour la touche majuscule à gauche, etc.

    À la différence des keycodes, les keysyms ne sont pas utilisés pour
    _identifier_ les touches physiques mais pour configurer le _résultat_ obtenu
    en pressant une touche. Ainsi, la _touche_ [Q]{.kbd} d’un clavier imprimé
    QWERTY peut être configurée pour produire le[^keysym-genre] keysym `q` ou
    `a` sur la couche de base, et les keysyms `Q` ou `A` sur la couche majuscule,
    etc.

: Il existe différents types de keysyms :

    - _caractère :_ `a` et `A` pour les scripts latins, `gamma` « γ » et `GAMMA`
      « Γ » pour le grec, etc.
    - _touche morte :_ `dead_grave` et `dead_diaeresis`, qui correspondent
      respectivement à l’accent grave et au tréma. Une touche morte est une
      touche spéciale car elle ne génère pas de caractère, mais modifie le
      caractère de la touche qui est utilisée directement après elle. Ce
      comportement nécessite la fonctionnalité « Compose ».
    - _modificateur :_ une touche qui modifie l’effet des autres touches : par
      exemple `Shift_L`, `Control_R`, `Caps_Lock`. Les modificateurs utilisent
      un mécanisme différent des touches mortes et servent à accéder aux
      différentes couches d’une disposition, ainsi qu’à définir des raccourcis
      clavier.
    - _système :_ actions spéciales non comprises ci-dessus : flèche `Left`,
      `Pause`, `Escape`, `F1`, etc.

Key type

: 🚧 définition à rajouter 🚧

Key Action

: 🚧 définition à rajouter 🚧

[Groupe]{#group-xkb-def}

: 🚧 définition à rajouter 🚧

: Également appelé abusivement _disposition_ (<i lang="en">layout</i>).
🚧 à développer 🚧

Keymap

: 🚧 définition à rajouter 🚧

[ISO/IEC 9995-2]: https://en.wikipedia.org/wiki/ISO/IEC_9995#ISO/IEC_9995-2
[input-event-codes.h]: https://github.com/torvalds/linux/blob/90d35da658da8cff0d4ecbb5113f5fac9d00eb72/include/uapi/linux/input-event-codes.h#L91

<!-- notes de bas de page -->
[^code-brut-noyau]: Correspond à `KEY_Q` dans le fichier d’en-tête
    [`input-event-code.h`][input-event-codes.h].
[^code-symbolique-iso-9995]: Les codes symboliques sont suivent la norme
    [ISO/IEC 9995-2] pour les touches alpha-numériques.
[^keysym-genre]: On devrait dire _un_ keysym car c’est un _symbole_ de touche,
    mais _une_ keysym sonne peut-être mieux.
