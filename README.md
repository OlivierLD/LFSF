# LFSF
Lycée Français de San Francisco

### Git basics
First, you need to clone the repository (aka `repo`):

From wherever you like on your disk, somewhere you will remember
```
$ git clone https://github.com/OlivierLD/LFSF.git
```
This will create a `LFSF` folder reflecting the content of the repo as it is on github.
By default, the branch is `master`. To see it:
```
$ cd LFSF
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
$
``` 

### Usefull git commands (to begin with)
```
$ git status
$ git pull origin master
$ git fetch
$ git log
```

There is also a legally free book about git that can be downloaded from [here](https://git-scm.com/book/en/v2).

#### Raspberry Pi, `/etc/rc.local` and friends
`/etc/rc.local` is a script executed *as `root`* _when the machine starts_.

This is typically where you would start the required servers, create symbolic links, this kind of things.

##### To start a command when opening the Graphical Desktop
This happens in `~/.config/lxsession/LXDE-pi/autostart`. Example:
```
@chromium-browser --incognito --kiosk [--force-device-scale-factor=0.90] http://localhost:9999/web/nmea/headup.html \
                                      [url.2] \
                                      [url.3] \
                                      [url.4]
```
In our case, it can also be a static resource like this:
```
@chromium-browser --incognito --kiosk file:///home/pi/LFSF/web/index.html
```
No running server seem to be reuiqred here.

> To know how to close tab, open tab, open window, etc, from the keyboard, look into the `File` menu of your Chrome browser.
> See in the `Window` menu how to navigate from tab to tab (Ctrl + Tab, Ctrl + Shft + Tab).
##### To prevent the desktop from going to sleep (no screen saver)
A Graphical Desktop will by default go to sleep if not solicited for a while, and we might not want that. To fix it:

- Edit `/etc/lightdm/lightdm.conf`
- Have a/the line that starts with `xserver-command=` to look like `xserver-command=X -s 0 -dpms`
- This will take effect after reboot.

### Usefull Software
- [Install Jupyter](https://jupyter.org/install)
- [Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- The **_best_** Python IDE: [Install PyCharm](https://www.jetbrains.com/help/pycharm/installation-guide.html)

To build a web site, hosted by github, see [**GitHub**Pages](https://pages.github.com/).

### Next
- [A carousel](https://www.w3schools.com/bootstrap/bootstrap_carousel.asp) ?

---

