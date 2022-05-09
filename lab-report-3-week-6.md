# ieng6 Configuration
> Author: Jeffrey Li \
This page showcases streamlining ssh configuration, Github access from ieng6, and copying directories with `scp`
___
## Streamlining ssh Configuration
### .ssh/config file that stores your ssh configuration on your local machine
**By adding your account information to .ssh/config, you are able to access your ieng6 account with a simple alias** \
![](/LabReport3/sshconfig.png)
### Logging in just using the alias you choose
**You can now log in just using a simple `ssh[alias]` command** \
![](/LabReport3/login.png)
### Using the scp command with just the alias you choose
**You can now use the alias you choose when using the `scp` command such as `scp filename alias destination`** \
![](/LabReport3/scpalias.png)
___
## Setup Github Access from ieng6
### Public Key on Github
**Select from personal settins on Github to add a new ssh key** \
![](/LabReport3/githubkey.png) 
### Public and Private Key on ieng6
**Using ssh-keygen on ieng6 to generate your ssh keys**
![](/LabReport3/ieng6key.png)
### Using git commands from ieng6
**In your repositary, you can use the git commit and git push commands to commit and push you changes for your repositiory** \
![](/LabReport3/gitcommit.png)
### Link to the Commit
[Commit](https://github.com/jeffreyli640/markdown-parser/commit/c32ce9a600dafeaedd6dd104a584bdfb1a7ea5ba)
___
## Comput whole directories with `scp -r`
### Using Multiple commands with scp and ssh and java
**The `-r` option with scp allows you to copy directories recursivley** \
**while the `;` command gives the option of combining multiple commands together.**
![](/LabReport3/scpr.png)