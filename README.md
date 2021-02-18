# Github Tricks
Section all about github use

# Github pages

### Github Pages - images not working
Attaching images to website while using GitHub Pages: https://www.elharony.com/images-not-displaying-in-github-pages/

## Github Branches

### Merging master into development branch 
```sh
git merge %branchname% master
```

### Pulling specific branch
```sh
git checkout --track origin/%branchname%
```

### Pulling master into development branch
```sh
git checkout %branchname%    # gets you on development branch  
  
git fetch origin        # gets you up to date with origin  
  
git merge origin/master  
```

## Pushing specific branch
```sh
git push --set-upstream origin %branchname%
```

## Deleting branch locally
```sh
git branch -d localBranchName
```

## Deleting branch remotely
```sh
git push origin --delete remoteBranchName
```

# Tailwind 

## Extending Default Color Pallete

```javascript
//tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        'regal-blue': '#243c5a',
      }
    }
  }
}
```
This will generate classes like `<bg-regal-blue>` in addition to all of Tailwind's default colors.

# Machine Setup

## Installing WSL
1. Open Windows PowerShell as Administrator and run command below, then reboot your PC.
```sh
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

2. After rebooting your computer, go to Microsoft Store and install Ubuntu.
![ubuntu image](https://www.computerhope.com/issues/pictures/wsl-store-2019.jpg)![ubuntu image](https://www.computerhope.com/issues/pictures/installwsl-store-get-ubuntu.jpg)

3. When WSL is installed, head to Visual Studio Code, press Crtl+Shift+P and type:`shell`

4. Now you can select WSL terminal as your default shell
## Installing nvm

To **install** or **update** nvm, you should run scripts below:
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```
```sh
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```

Running either of the above commands downloads a script and runs it. The script clones the nvm repository to `~/.nvm`, and attempts to add the source lines from the snippet below to the correct profile file (`~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`).

<a id="profile_snippet"></a>
```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

## Installing node 
```sh
nvm install v%nodeversion%
```

## Installing npm 
```sh
npm install npm@latest -g
```

## Installing yarn
```sh
curl -o- -L https://yarnpkg.com/install.sh | bash
```

Restart terminal and test with command below
```sh
yarn --version
```

## Installing git
```sh
sudo apt install git-all
```

## Setting up .ssh
Run commands below in bash  

```sh
ssh-keygen -t ed25519 -C "your_email@example.com"  
```

After these steps copy `id_ed25519.pub` to your github account  
