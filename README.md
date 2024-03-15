# Flora

An end to end encrypted chat room using GPG's AES256 cypher, supporting multiple users written entirely in bash with the help of socat.

Dependencies:
-
bash

socat

gpg

Ussage:
-

```
git clone https://github.com/Tina-lel/Flora
```

```
cd Flora
```

```
chmod +x flora
```

see ```./flora -h``` for a list of arguments

## server:

set an encryption password using:

```
./flora -p
```

the password file was generated in ~/.config/flora/server/pass you should be careful with it (ITS PLAIN TEXT)

you may set custom ports as well as a custom motd message in ~/.config/flora/server.cfg

then start the server using:

```
./flora -s
```

enter "help" for a list of valid commands

if everything went fine, and the server didn't return any errors, you can test the connection with a client

## client:

```
./flora
```

Feel free to edit the "# GENERAL CONFIG" and "# KEYBINDS" part of the config in ~/.config/flora/client.cfg, to set a new user name or user color for example.

Refrain from changing anything in the "# SERVER CONFIG" part though, as this is mostly managed by the script itself. You can however delete no longer wanted servers by deleting their entry in the "FUNCS" array, as well as their respective function

To connect to a server hit "Add" in the newly opened Menu, and fill out the info to match the info of a server currently running the server script. After that it should pop up in the Menu. Select it, press enter, and input the password to connect.

If everything went fine you should be seeing a motd message, press q to get to the chatbox. (!h for a list of commands)
