# SSH

## Check for current keys 

`ls –al ~/.ssh`

## Create SSH Key 

`ssh-keygen –t rsa –b 4096 –C YOURGITHUBEMAIL@PLACEHOLDER.NET`
or
`ssh-keygen -t ed25519 -C YOURGITHUBEMAIL@PLACEHOLDER.NET`
*dont create a pass phrase*

**Mac Users: try this if the above command is not working**

`ssh-keygen -t rsa`

Press `enter` to default to root directory 

Press `enter` to not use a passphrase 

Press `enter` again to not use a passphrase 

## Check that ssh agent is running 

`eval $(ssh-agent –s)`

## Link key to machine 

`ssh-add ~/.ssh/id_rsa`
`ssh-add ~/.ssh/id_ed25519`

### Copy to clipboard  

`clip < ~/.ssh/id_rsa.pub`
`clip < ~/.ssh/id_ed25519.pub`

**Mac**

`pbcopy < ~/.ssh/id_rsa.pub`

No feedback while be given that this worked 🤷

### Paste in GitHub Account

* Go to GitHub account => Settings => SSH and GPG Keys => New SSH Key
* Paste in SSH key
