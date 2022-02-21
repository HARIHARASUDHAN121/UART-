# Kernel Flashing via Boot-Console
This method can be done by using `Teraterm` but here we using the `software protocol`(i.e) `lrzsz` this we can done in the terminal itself.
## STEPS for kernel flashing:
### Step-1: Install lrzsz
To install lrzsz give this command
```
sudo apt install -y lrzsz
```
### Step-2: Connect the board 
 * Connecting the board to PC via normal putty port and also open the putty.
 * Then give the command `loady` in the putty console.
 
 Note - `loady` for `ymodem` module, `loadx` for `xmodem` module, `loadz` for `zmodem` module.
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

 


