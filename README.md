#CM Storm Devastator OSX
A dead simple way to turn CM Storm Devastator Keyboard On and Off with Keyboard Shortcuts on OSX

### Setup

#### 1) Clone this repo or download the zip from the link here.

In terminal
```shell
git clone https://github.com/dannyvassallo/cm-storm-devastator.git
```

#### 2) Copy and paste the ```led-backlight-osx``` into your ```Applications``` folder.

#### 3) Chmod ```led-backlight-osx``` you will need to enter your admin pass.

In terminal
```shell
cd /Applications/
sudo chmod u+x ./led-backlight-osx
```
### Turning the Keyboard's backlight ON

#### 4) Launch the OS X "Automator" program

#### 5) Choose "Service" document type

#### 6) Under "Library", click "Utilities", and drag "Run Shell Script" to the blank area / workflow pane.

#### 7) For "selected service receives" choose "no input" in "any application" (important)

#### 8) For "pass input" choose "as arguments" (important)

#### 9) For "shell" choose "/bin/bash"

#### 10) Paste in this script:

```
cd /Applications
./led-backlight-osx
```

#### 11) Click "run" to test. After 3 seconds, your keyboard should remain in a state with num lock and scroll lock enabled, and all the keys should be lit up. Yay! Continue to assign keyboard shortcut to do this.

#### 12) Click "File" > "Save", "Save service as" : "Devastator LED Lighter ON

#### 13) Go to System Preferences > Keyboard > Shortcuts > Services > General > "Devastator LED Lighter ON"

#### 14) Assign a key shortcut to turn the keyboard on.


### Turning the Keyboard's backlight OFF


#### 15) In "Automator" goto File > New

#### 16) Choose "Service" document type

#### 17) Under "Library", click "Utilities", and drag "Run Shell Script" to the blank area / workflow pane.

#### 18) For "selected service receives" choose "no input" in "any application" (important)

#### 19) For "pass input" choose "as arguments" (important)

#### 20) For "shell" choose "/bin/bash"

#### 21) Paste in this script:

```
cd /Applications
./led-backlight-osx off
```

#### 22) Click "run" to test. After 3 seconds, your keyboard's backlight should turn off.

#### 23) Click "File" > "Save", "Save service as" : "Devastator LED Lighter OFF

#### 24) Go to System Preferences > Keyboard > Shortcuts > Services > General > "Devastator LED Lighter OFF"

#### 25) Assign a key shortcut to turn the keyboard off.


Build borrowed from: (https://github.com/pykler/led-backlight-osx)[https://github.com/pykler/led-backlight-osx]
Thanks pykler!
