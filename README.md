# Github Tricks
Section all about github use

# Github pages

### Github Pages - images not working
Attaching images to website while using GitHub Pages: https://www.elharony.com/images-not-displaying-in-github-pages/

## Github Branches

### Pulling specific branch
git checkout --track origin/%branchname%

### Pulling master into development branch
git checkout %branchname%    # gets you on development branch  
  
git fetch origin        # gets you up to date with origin  
  
git merge origin/master  

## Pushing specific branch
git push --set-upstream origin %branchname%

## Deleting branch locally
git branch -d localBranchName

## Deleting branch remotely
git push origin --delete remoteBranchName

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
nvm install v%nodeversion%

## Installing npm 
npm install npm@latest -g

## Installing yarn
sudo npm install -g yarn

## Installing git
sudo apt install git-all
