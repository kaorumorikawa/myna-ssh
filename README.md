# myna-ssh
ssh authentication using Japanese MyNumber Card on Windows

This program extracts User Authentication Public Key on MyNumber card in ssh-key format.

It prints the ssh-key on the screen. Copy the key and paste it to the file authorized_key 
in .ssh directory under a user's home folder

On a client computer, assuming that a IC card reader is up and running to read MyNumber card,
run pagaent.exe from puTTY-CAC, add "PKCS certs" using OpenSC pkcs11 module and select 
User Authentication Certificate on MyNumber card. Be sure to set Finterprint Type to
"SHA256 including".

Run a ssh client that supports authentication via pagaent. Such clients include WinSCP and
Teraterm. Log in as the user for whose home folder's .ssh authentication file you have
pasted the ssh-key. You must configure your ssh client to use pagaent for authentication.


