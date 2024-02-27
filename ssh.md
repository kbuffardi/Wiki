### Setting Up SSH Keys in ECC-Linux

Setting up SSH Keys is a fairly simple procedure to authenticate to ECC-Linux

#### MacOS / Linux Instructions

1. Connect to the VPN ([Instructions](/vpn))
2. Create an SSH Public / Private Key
   
   `ssh-keygen -b 4096 -t rsa`

3. You can view your SSH Keys with the following command

   `cat ~/.ssh/id_rsa.pub`

4. There are two ways to copy this key onto the remote server

##### Using `ssh-copy-id`
Run the command `ssh-copy-id <SERVER NAME>`

##### Adding SSH key to Remote Server

