# pop OS Configuration
Configuration of Pop OS based on my preference 
# apt packages
 - neofetch : show system info
 - thermald : daemon cpu monitor
 - terminator : alternative terminal
 - auto-cpufreq : manage cpu to 
 - nvnm : node version manager
 - zsh : bash alternative
 - vim : vi Improved

```bash
sudo apt update
sudo apt upgrade
sudo apt dist-upgrade
sudo apt autoremove
sudo apt autoclean
sudo fwupdmgr get-devices
sudo fwupdmgr get-updates
sudo fwupdmgr update
flatpak update
sudo apt install neofetch
sudo apt install thernald
sudo apt install vim
sudo pop-upgrade recovery upgrade from-release # this updates the recovery partition





# install custom fonts


# configuration zsh 
curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${Zsh_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k


```

# Flatpack 
```bash
# Get list of flatpak installed
flatpak list --app --show-details | \
awk '{print "flatpak install --assumeyes --user \""$2"\" \""$1}' | \
cut -d "/" -f1 | awk '{print $0"\""}'

flatpak install --assumeyes --user "Gérer" "Flatseal"
flatpak install --assumeyes --user "Chrome" "Google"
flatpak install --assumeyes --user "d’extensions" "Gestionnaire"
flatpak install --assumeyes --user "Edge" "Microsoft"
flatpak install --assumeyes --user "VPN" "Proton"
flatpak install --assumeyes --user "Desktop" "GitHub"
flatpak install --assumeyes --user "Cleans" "BleachBit"
flatpak install --assumeyes --user "Powerful" "Flameshot"
flatpak install --assumeyes --user "Prise" "Cheese"
```


# Node packages

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
nvm install --lts
nvm use --lts
curl -fsSL https://get.pnpm.io/install.sh | sh -
echo 'alias pn=pnpm' >> ~/.zshrc
source ~/.zshrc

pn add -g prettier eslint typescript protractor

```


# dconf

dump and load 
```
conf dump / > dconf-settings.ini
dconf load / < dconf-settings.ini

```

```bash
[com/gexperts/Tilix]
quake-specific-monitor=0

[com/gexperts/Tilix/profiles/2b7c4080-0ddd-46c5-8f23-563fd3ba789d]
font='MesloLGS NF 12'
use-system-font=false
visible-name='Par défaut'

[com/github/donadigo/eddy]
mime-types=['application/vnd.debian.binary-package', 'application/x-deb']
window-x=150
window-y=182

[io/elementary/appcenter/settings]
cached-drivers=@as []
last-refresh-time=int64 1705673745
window-maximized=false
window-size=(1904, 960)

[org/gnome/Geary]
migrated-config=true

[org/gnome/Weather]
automatic-location=false
locations=[<(uint32 2, <('Paris', 'LFPB', true, [(0.85462956287765413, 0.042760566673861078)], [(0.8528842336256599, 0.040724343395436846)])>)>]

[org/gnome/calculator]
accuracy=9
angle-units='degrees'
base=10
button-mode='basic'
number-format='automatic'
show-thousands=false
show-zeroes=false
source-currency=''
source-units='degree'
target-currency=''
target-units='radian'
window-position=(100, 132)
word-size=64

[org/gnome/control-center]
last-panel='bluetooth'

[org/gnome/desktop/a11y/interface]
high-contrast=false

[org/gnome/desktop/a11y/magnifier]
mag-factor=1.75
mouse-tracking='proportional'

[org/gnome/desktop/app-folders/folders/Pop-Office]
apps=['libreoffice-calc.desktop', 'libreoffice-draw.desktop', 'libreoffice-impress.desktop', 'libreoffice-math.desktop', 'libreoffice-startcenter.desktop', 'libreoffice-writer.desktop']
name='Office'
translate=true

[org/gnome/desktop/app-folders/folders/Pop-System]
apps=['gnome-language-selector.desktop', 'gnome-session-properties.desktop', 'gnome-system-monitor.desktop', 'im-config.desktop', 'nm-connection-editor.desktop', 'nvidia-settings.desktop', 'org.gnome.baobab.desktop', 'org.gnome.DiskUtility.desktop', 'org.gnome.PowerStats.desktop', 'org.gnome.seahorse.Application.desktop', 'software-properties-gnome.desktop', 'system76-driver.desktop', 'system76-firmware.desktop']
name='System'
translate=true

[org/gnome/desktop/app-folders/folders/Pop-Utility]
apps=['com.github.donadigo.eddy.desktop', 'com.system76.Popsicle.desktop', 'gucharmap.desktop', 'info.desktop', 'org.gnome.eog.desktop', 'org.gnome.Evince.desktop', 'org.gnome.Extensions.desktop', 'org.gnome.FileRoller.desktop', 'org.gnome.font-viewer.desktop', 'org.gnome.Screenshot.desktop', 'org.gnome.Totem.desktop', 'pop-cosmic-applications.desktop', 'pop-cosmic-launcher.desktop', 'pop-cosmic-workspaces.desktop', 'simple-scan.desktop', 'yelp.desktop']
name='Utilities'
translate=true

[org/gnome/desktop/background]
color-shading-type='solid'
picture-options='zoom'
picture-uri='file:///usr/share/backgrounds/pop/benjamin-voros-250200.jpg'
primary-color='#000000'
secondary-color='#000000'

[org/gnome/desktop/calendar]
show-weekdate=false

[org/gnome/desktop/datetime]
automatic-timezone=false

[org/gnome/desktop/input-sources]
current=uint32 0
mru-sources=[('xkb', 'us'), ('xkb', 'fr')]
per-window=false
show-all-sources=false
sources=[('xkb', 'fr'), ('xkb', 'us')]
xkb-options=@as []

[org/gnome/desktop/interface]
clock-format='24h'
clock-show-seconds=true
clock-show-weekday=true
color-scheme='prefer-light'
cursor-size=48
enable-hot-corners=true
font-antialiasing='rgba'
font-hinting='full'
font-name='Fira Sans Light 11'
gtk-theme='Pop'
locate-pointer=true
show-battery-percentage=true

[org/gnome/desktop/notifications]
application-children=['gnome-control-center', 'gnome-power-panel', 'gnome-network-panel', 'io-elementary-appcenter', 'flatpak-installer', 'com-github-donadigo-eddy', 'gnome-datetime-panel', 'firefox', 'jetbrains-toolbox', 'jetbrains-datagrip-87c943d8-7ace-46bc-a855-4d78d5101358', 'jetbrains-webstorm-597e0eeb-be40-4c5a-867b-0511ecd259ab', 'org-gnome-nautilus', 'org-gnome-fileroller', 'org-gnome-tweaks']
show-banners=false

[org/gnome/desktop/notifications/application/com-github-donadigo-eddy]
application-id='com.github.donadigo.eddy.desktop'

[org/gnome/desktop/notifications/application/firefox]
application-id='firefox.desktop'

[org/gnome/desktop/notifications/application/flatpak-installer]
application-id='flatpak-installer.desktop'

[org/gnome/desktop/notifications/application/gnome-control-center]
application-id='gnome-control-center.desktop'

[org/gnome/desktop/notifications/application/gnome-datetime-panel]
application-id='gnome-datetime-panel.desktop'

[org/gnome/desktop/notifications/application/gnome-network-panel]
application-id='gnome-network-panel.desktop'

[org/gnome/desktop/notifications/application/gnome-power-panel]
application-id='gnome-power-panel.desktop'

[org/gnome/desktop/notifications/application/io-elementary-appcenter]
application-id='io.elementary.appcenter.desktop'

[org/gnome/desktop/notifications/application/jetbrains-datagrip-87c943d8-7ace-46bc-a855-4d78d5101358]
application-id='jetbrains-datagrip-87c943d8-7ace-46bc-a855-4d78d5101358.desktop'

[org/gnome/desktop/notifications/application/jetbrains-toolbox]
application-id='jetbrains-toolbox.desktop'

[org/gnome/desktop/notifications/application/jetbrains-webstorm-597e0eeb-be40-4c5a-867b-0511ecd259ab]
application-id='jetbrains-webstorm-597e0eeb-be40-4c5a-867b-0511ecd259ab.desktop'

[org/gnome/desktop/notifications/application/org-gnome-fileroller]
application-id='org.gnome.FileRoller.desktop'

[org/gnome/desktop/notifications/application/org-gnome-nautilus]
application-id='org.gnome.Nautilus.desktop'

[org/gnome/desktop/notifications/application/org-gnome-tweaks]
application-id='org.gnome.tweaks.desktop'

[org/gnome/desktop/peripherals/mouse]
speed=0.38970588235294112

[org/gnome/desktop/peripherals/touchpad]
natural-scroll=true
speed=0.52205882352941169
two-finger-scrolling-enabled=true

[org/gnome/desktop/privacy]
report-technical-problems=false

[org/gnome/desktop/screensaver]
color-shading-type='solid'
lock-delay=uint32 0
picture-options='zoom'
picture-uri='file:///usr/share/backgrounds/pop/benjamin-voros-250200.jpg'
primary-color='#000000'
secondary-color='#000000'

[org/gnome/desktop/session]
idle-delay=uint32 300

[org/gnome/desktop/sound]
allow-volume-above-100-percent=false

[org/gnome/desktop/wm/preferences]
button-layout='close,minimize,maximize:appmenu'

[org/gnome/evolution-data-server]
migrated=true
network-monitor-gio-name=''

[org/gnome/file-roller/listing]
list-mode='as-folder'
name-column-width=250
show-path=false
sort-method='name'
sort-type='ascending'

[org/gnome/file-roller/ui]
sidebar-width=200
window-height=429
window-width=948

[org/gnome/gedit/plugins]
active-plugins=['docinfo', 'filebrowser', 'sort', 'modelines', 'spell', 'openlinks']

[org/gnome/gedit/plugins/filebrowser]
root='file:///'
tree-view=true
virtual-root='file:///home/radnoumanemossabely/T%C3%A9l%C3%A9chargements/AnonymousPro'

[org/gnome/gedit/preferences/editor]
scheme='pop-light'

[org/gnome/gedit/preferences/ui]
show-tabs-mode='auto'

[org/gnome/gedit/state/window]
bottom-panel-size=140
side-panel-active-page='GeditWindowDocumentsPanel'
side-panel-size=200
size=(900, 700)
state=87168

[org/gnome/gnome-system-monitor]
current-tab='processes'
maximized=false
network-total-in-bits=false
show-dependencies=false
show-whose-processes='user'
window-state=(700, 500, 50, 50)

[org/gnome/gnome-system-monitor/disktreenew]
col-6-visible=true
col-6-width=0

[org/gnome/gnome-system-monitor/proctree]
columns-order=[0, 1, 2, 3, 4, 6, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26]
sort-col=22
sort-order=0

[org/gnome/mutter]
center-new-windows=true
edge-tiling=false

[org/gnome/nautilus/icon-view]
captions=['type', 'date_accessed', 'none']

[org/gnome/nautilus/list-view]
use-tree-view=true

[org/gnome/nautilus/preferences]
default-folder-viewer='icon-view'
search-filter-time-type='last_modified'
search-view='list-view'
show-delete-permanently=false

[org/gnome/nautilus/window-state]
initial-size=(890, 550)
maximized=false
sidebar-width=225

[org/gnome/power-manager]
info-history-graph-smooth=true
info-history-time=86400
info-history-type='rate'
info-last-device='/org/freedesktop/UPower/devices/battery_BAT0'
info-page-number=2
info-stats-graph-points=true
info-stats-type='discharge-accuracy'

[org/gnome/settings-daemon/plugins/color]
night-light-enabled=true
night-light-last-coordinates=(48.840201439884808, 2.3386999999999998)
night-light-schedule-automatic=true
night-light-temperature=uint32 3700

[org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/PopLaunch1]
binding='Launch1'
command='gnome-control-center wifi'
name='WiFi'

[org/gnome/settings-daemon/plugins/power]
sleep-inactive-ac-timeout=1800
sleep-inactive-ac-type='suspend'
sleep-inactive-battery-timeout=1800
sleep-inactive-battery-type='suspend'

[org/gnome/shell]
disable-user-extensions=false
disabled-extensions=@as []
enabled-extensions=['ding@rastersoft.com', 'pop-cosmic@system76.com', 'pop-shell@system76.com', 'ubuntu-appindicators@ubuntu.com', 'cosmic-dock@system76.com', 'cosmic-workspaces@system76.com', 'popx11gestures@system76.com', 'system76-power@system76.com']
favorite-apps=['pop-cosmic-launcher.desktop', 'pop-cosmic-workspaces.desktop', 'pop-cosmic-applications.desktop', 'org.gnome.Nautilus.desktop', 'com.microsoft.Edge.desktop', 'com.gexperts.Tilix.desktop', 'jetbrains-webstorm-597e0eeb-be40-4c5a-867b-0511ecd259ab.desktop']
welcome-dialog-last-shown-version='42.5'

[org/gnome/shell/extensions/dash-to-dock]
click-action='minimize-or-previews'
dash-max-icon-size=48
dock-alignment='CENTER'
dock-fixed=true
extend-height=false
intellihide=false
manualhide=false

[org/gnome/shell/extensions/ding]
sort-special-folders=true

[org/gnome/shell/extensions/pop-cosmic]
clock-alignment='CENTER'
workspace-picker-left=false

[org/gnome/shell/extensions/pop-shell]
tile-by-default=true

[org/gnome/shell/weather]
automatic-location=false
locations=[<(uint32 2, <('Paris', 'LFPB', true, [(0.85462956287765413, 0.042760566673861078)], [(0.8528842336256599, 0.040724343395436846)])>)>]

[org/gnome/system/location]
enabled=true

[org/gnome/terminal/legacy/profiles:]
default='a378e100-0dc5-4a93-827c-8c45a0cecbd9'
list=['b1dcc9dd-5262-4d8d-a863-c897e6d979b9', 'a378e100-0dc5-4a93-827c-8c45a0cecbd9']

[org/gnome/terminal/legacy/profiles:/:a378e100-0dc5-4a93-827c-8c45a0cecbd9]
font='MesloLGS NF 12'
visible-name='rad'

[org/gtk/settings/file-chooser]
clock-format='24h'
date-format='regular'
location-mode='path-bar'
show-hidden=true
show-size-column=true
show-type-column=true
sidebar-width=184
sort-column='name'
sort-directories-first=true
sort-order='ascending'
type-format='category'
window-position=(412, 85)
window-size=(1096, 822)

```
