# sway

sway este un compositor pentru [Wayland](http://wayland.freedesktop.org/) compatibil cu [i3](https://i3wm.org/).
Citiți [FAQ](https://github.com/swaywm/sway/wiki)-ul. Connectați-vă la canalul nostru [IRC](http://webchat.freenode.net/?channels=sway&uio=d4) (#sway pe irc.freenode.net).

Dacă doriți să contribuiți la dezvoltarea sway, vă rugăm contribuiți în [pagina de Patreon lui SirCmpwn](https://patreon.com/sircmpwn).

## Semnarea digitală

Noile versiuni sunt semnate cu [B22DA89A](http://pgp.mit.edu/pks/lookup?op=vindex&search=0x52CB6609B22DA89A)
și postate [pe GitHub](https://github.com/swaywm/sway/releases).

## Instalare

### Din pachete (packages) 

sway este valabil în multe distribuții. încercați a instala "sway" pe distribuția voastră. Dacă nu este valabil, uitați-vă în [această pagină wiki](https://github.com/swaywm/sway/wiki/Unsupported-packages)
pentru informații a cum puteți să instalați pentru distribuția voastră.

Dacă sunteți interesați in a crea pachete pentru distribuția voastră, informați-ne prin IRC sau contactați prin email pe sir@cmpwn.com pentru ajutor.

### Construire din sursă

Dependențe pentru instalare:

* meson \*
* [wlroots](https://github.com/swaywm/wlroots)
* wayland
* wayland-protocols \*
* pcre
* json-c
* pango
* cairo
* gdk-pixbuf2 (optional: system tray)
* [scdoc](https://git.sr.ht/~sircmpwn/scdoc) (optional: pagini man) \*
* git (optional: info versiune) \*

*Dependențe doar pentru compilare*

Rulați aceste comenzi:

```
    meson build
    ninja -C build
    sudo ninja -C build install
```

Pe sisteme fără logind, trebuie făcut următorul:

```
    sudo chmod a+s /usr/local/bin/sway
```
Sway o să scape de permisiuni root la puțin timp după lansare.

## Configurare

Dacă folosiți deja i3, copiați fișierul de configurare din i3 în `~/.config/sway/config`, și va funcționa fără a necesita nici o modificare. In caz contrar, copiați exemplul de configurare (disponibil de obicei în `/etc/sway/config`) în `~/.config/sway/config`.
Folosiți comanda `man 5 sway` pentru informații despre configurare.

## Lansare

Folosiți comanda `sway` într-un TTY. Managerii de display nu sunt suportați de către Sway, dar unii pot functiona (se știe că gdm functioneazâ destul de bine).
