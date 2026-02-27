# Connect your local repository Git with GitHub on Linux 
1. Create a ssh key
    $ ssh-keygen -t ed25519 -C "nokus@live.fr"
2. Start the ssh-agent in the background
    $ eval "$(ssh-agent -s)"
3. Add your SSH private key to the ssh-agent.
    $ ssh-add ~/.ssh/id_ed25519
4. Copy your SSH public key to your GitHub account
    $ cat ~/.ssh/id_ed25519.pub
    # Then select and copy the contents of the id_ed25519.pub file
    # displayed in the terminal to your clipboard
5. Past your SSH public key on your GitHub Account
    Go to https://github.com/settings/keys
    Select New SSH Key
    Give it a Title and in the field Key, Past the SSH public key you copied at the previous step.
6. Test the connection to your GitHub
    $ ssh -T git@github.com
    # The origin should be already define before that

# Define an origin on Linux
    $git remote set-url origin git@github.com:<Your GitHup Username>/<Your Remote repository>
    # You can test the configuration with 