# Kernel Flashing via Boot-Console
This method is used to transfer files and it is done by using `Teraterm` option which are build-in with that software. But in linux, we use `putty` which has no provision like this. Therefore, we use `lrzsz` in the terminal for tranfering files.
## STEPS for kernel flashing:
### Step-1: Install lrzsz
To install lrzsz give this command
```
sudo apt install -y lrzsz
```
### Step-2: Connect the board 
 * Connecting the board to PC via normal putty port and also open the putty.
 * Make sure of the module you use (xmodem, ymodem)
 * Then give the command `loady` in the putty console.
 
 Note - `loady` for `ymodem` module, `loadx` for `xmodem` module.
### Step-3: 
 * In terminal, need to set some parameters,
 ```
 $sudo chmod 666 /dev/ttyUSB0
 $DEV=/dev/ttyUSB0
 $BAUDRATE=115200
 ```
 * Then give these cmd,
 ```
 $sudo stty -F $DEV $BAUDRATE
 $Sb <filename> >$DEV <$DEV
 ```
 here, `sb` for `ymodem`, `sx` for `xmodem`, `sz` for `zmodem`.

 


