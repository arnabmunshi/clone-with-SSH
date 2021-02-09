## Add SSH key on github

### Step #1
- Open Bash Terminal
- [Reference](https://git.io/JeuCN)
- `ssh-keygen -t rsa -b 4096 -C "<Your GitHub Email ID>"`

### Step #2
- Enter file in which to save the key
- Default is `id_rsa` or if you want change the type
- `/<DRIVE>/Users/<Username>/.ssh/<id_rsa_test>`

### Step #3
- Enter passphrase <press enter>
  
### Step #4
- Enter same passphrase again: <pree enter>
  
### Step #5
- Start the ssh-agent in the background
- `eval $(ssh-agent -s)`

### Step #6
- Add your SSH private key to the ssh-agent.
- `ssh-add ~/.ssh/<id_rsa_test>`

### Step #7
- Add SSH key to Github account
- [Reference](https://git.io/JfKid)
- Copy the SSH key on clipboard
- `clip < ~/.ssh/<id_rsa_test.pub>`

### Step #8
- Open this link on your browser
- [Link](https://github.com/settings/keys)
- Click "New SSH key" button
- Give a Title Like: <Office Desktop>
- And paste key on the key Textarea
- Click "Add SSH key" button
- Now your newly crated SSH key icon is "Gray"

## Testing your SSH connection
`ssh -T git@github.com`

## Clone GitHub Repo With SSH
- [Reference](https://www.youtube.com/watch?v=3aKda-oXWc8)
- Open your project directory
- Open your bash terminal on same project directory
- `eval $(ssh-agent -s)`
- `ssh-add ~/.ssh/<id_rsa_test>`
- `git clone git@github.com:arnabmunshi/Clone-With-SSH.git`
- Now your newly crated SSH key icon turn into "Green"

Used [git.io](git.io) to short git url
