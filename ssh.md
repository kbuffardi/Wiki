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
Run the command `ssh-copy-id -i ~/.ssh/id_rsa.pub <USER@SERVER_NAME>`

You should now be able to authenticate to your host machine without a password

##### Adding SSH key to Remote Server Manually

1. On your local machine run `cat ~/.ssh/id_rsa.pub`
2. Copy the entire file
3. On the host machine run `vim ~/.ssh/authorized_keys`
4. Copy the your public key into a new line

You should now be able to authenticate to your host machine without a password




