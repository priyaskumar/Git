SSH Keys
===

Can connect to GitHub using the Secure Shell Protocol (SSH), which provides a secure channel over an unsecured network.

### **_Why SSH Keys?_**


  * Can connect and authenticate to remote servers and services. 
  * Can connect to GitHub without supplying username and personal access token at each visit.

### **_Setting up SSH_**

  * Generate a new SSH key and add it to the ssh-agent.
  * Can further secure your SSH key by using a hardware security key (requires the physical hardware security key to be attached to the computer)

### **_Checking for existing SSH keys_**

Before you generate an SSH key, you can check to see if you have any existing SSH keys.

  * Open Git Bash.
  * Enter ls -al ~/.ssh to see if existing SSH keys are present.
    ```
    $ ls -al ~/.ssh
    # Lists the files in your .ssh directory, if they exist
    ```
  * Check the directory listing to see if you already have a public SSH key. By default, the filenames of supported   public keys for GitHub are one of the following.
    ```
    id_rsa.pub
    id_ecdsa.pub
    id_ed25519.pub
    ```
  * Either generate a new SSH key or upload an existing key.

### **_Generating a new SSH key_**

After you've checked for existing SSH keys, you can generate a new SSH key to use for authentication

  * Open Git Bash.
  * Type the following command in the terminal.
    ```
    $ ssh-keygen -t ed25519 -C "your_email@example.com"
    ```
    Note: If you are using a legacy system that doesn't support the Ed25519 algorithm, use:
    ```
    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```
    This creates a new SSH key, using the provided email as a label.
    ```
    > Generating public/private algorithm key pair.
    ```
  * When prompted to "Enter a file in which to save the key," press Enter. (accepts the default file location)
    ```
    > Enter a file in which to save the key (/c/Users/you/.ssh/id_algorithm):[Press enter]
    ```
  * At the prompt, type a secure passphrase. 
    ```
    > Enter passphrase (empty for no passphrase): [Type a passphrase]
    > Enter same passphrase again: [Type passphrase again]
    ```
### **_Adding SSH Key to the ssh-agent_**

  * To ensure the ssh-agent is running type the following command.
    ```
    # start the ssh-agent in the background
    $ eval "$(ssh-agent -s)"
    ```
    This will result in..
    ```
    > Agent pid 59566
    ```
  * Add SSH private key to the ssh-agent.
    ```
    $ ssh-add ~/.ssh/id_ed25519
    ```
  * Add the SSH key to the account on GitHub

<p align="center">
<img src="https://user-images.githubusercontent.com/94846381/143044695-95c7ae26-3a09-4c89-9afd-cd6101ef26d3.png"width="600" title="ssh">
</p>



