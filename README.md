# Rebuild my Ubuntu

## connect to SJTU using Jaccount

choose SJTU

1. set `Authentication` to `Protected EAP(PEAP)`

2. choose `No CA certificate is required`

3. set `Inner autentication` to `MSCHAPv2`

4. input username and password.

![wifi-setting](./assets/wifi-setting.png)

## set apt-get server

go to `System Settings -> Software & Updates` choose the Download from server.

## Git

1. `sudo apt-get install git`

2. Then add following scripts in .bashrc:

```
# git
alias gc='git commit -am'
alias gps='git push'
alias gpl='git pull'
alias ga='git add'
alias gs='git status'
```

3. set git configs on ids

```
git config --global user.email "imbaguanxin@
```

## Sogou Pinyin

1. dependencies

```
sudo apt-get install fcitx fcitx-config-gtk fcitx-table-all im-switch
sudo apt-get install libopencc1 fcitx-libs fcitx-libs-qt fonts-droid-fallback
```

2. install Chinese support

go to `System Settings -> Language Support -> Install/Remove Language -> install Chinese`

3. config Input Method

Since Sogou Pinyin is built on `Fcitx`, we need to change the input method to fcitx instead of default methods (probably IBUS).

* go to `Input Method Configuration`

```
im-config
```
press `ok` -> `yes` -> select fcitx -> `ok` -> `ok`

then reboot the system
```
sudo reboot
```

4. install sogou

go to the official cite of sogou pinyin linux version and download the source.

install the .deb package

```
sudo dpkg -i sogoupinyin_*.deb
```

This may result in errors since some dependencies are not installed.

use following command to fix (please refer to the warning/error message and the instructions on fixing the problem provided by system).

```
sudo apt-get -f install
```

4. config fcitx and sogou

go to Fcitx Configuration

```
fcitx-config-gtk3
```

***OR*** search `fcitx configuration` in applications

Press the `Plus` button at the lower left conner and search for `sogou`. Then add `Sogou Pinyin`  as input method.

Then reboot computer. All should be fine now.

## install Java




