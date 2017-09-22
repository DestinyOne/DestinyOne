## Letting ubuntu bash on Windows 10 run 'ssh -X'  to get a GUI environment in a remote server

#First
Intall all the following. On Window, install Xming. On Ubuntu bash, use 'sudo apt install' to install 'ssh sshd xauth xorg'.
Second, go to the folder contains 'ssh_config' file, mine is '/etc/ssh'.
Third, edit 'ssh_config' as administrator. Inside 'ssh_config', remove the hash '#' in the lines 'ForwardAgent', 'ForwardX11', 'ForwardX11Trusted', and set the corresponding arguments to 'yes'.
Forth, in 'ssh_config' file, remove the front hash '#' before 'Port 22' and 'Protocol 2', and also append a new line at the end of the file to state the xauth file location, 'XauthLocaion /usr/bin/xauth', remember write your own path of xauth file.
Fifth, now since we are done editing 'ssh_config' file, save it when we leave the editor. Now go to folder '~' or '$HOME', append 'export DISPLAY=localhost:0' to your '.bashrc' file and save it.
Last, we are almost done. Restart your bash shell, open your Xming program and use 'ssh -X yourusername@yourhost'. Then enjoy the GUI environment.