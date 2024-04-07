### New Mac Setup Checklist:

#### Software Installation:

1. **Homebrew:** Install Homebrew package manager.
    - Website: [brew.sh](https://brew.sh/)
    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

    Make sure to follow the instructutions at the end - there is something to ensure it gets added to the `$PATH`

2. **oh-my-zsh:** Install oh-my-zsh for enhanced terminal experience.
    - Website: [ohmyz.sh](https://ohmyz.sh/#install)
    ```bash
    sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```

3. **AWS CLI:** Install AWS Command Line Interface.
    - Documentation: [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
   ```bash
   curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
   sudo installer -pkg AWSCLIV2.pkg -target /
   ```

4. **Pyenv:** Python version management tool.
    ```bash
    brew install pyenv
    ```

5. **Poetry:** Python dependency management and packaging tool.
    ```bash
    brew install poetry
    ```

6. **MySQL:** 
    ```bash
    brew install mysql
    ```

7. **Node.js & npm:** JavaScript runtime and package manager. allows you to run `npm`
    ```bash
    brew install node
    ```

8. **Databricks CLI:** 
    - Documentation: [Databricks CLI Installation Guide](https://docs.databricks.com/en/dev-tools/cli/install.html#homebrew-install)
    ```bash
    brew tap databricks/tap
    brew install databricks
    ```

9. **Amplify CLI:** Command-line interface for AWS Amplify.
    ```bash
    npm install -g @aws-amplify/cli
    ```

#### Verification:

- To verify installed packages, run `brew list` in the terminal.
- Git should already be installed. You can verify by running `git --version`.
If you get a git not found error:
```
brew install git
```

### Recommended Software for Mac Setup:

1. **Visual Studio Code (VSCode):**
    - Website: [Visual Studio Code](https://code.visualstudio.com/)
    ```bash
    brew install --cask visual-studio-code
    ```

2. **PyCharm (Community Edition):**
    - Download the Toolbox and use the Interface to manage apps from there.
    - Website: [JetBrains Toolbox](https://www.jetbrains.com/toolbox-app/)

3. **Docker:**
    - Website: [Docker](https://www.docker.com/products/docker-desktop)
    ```bash
    brew install --cask docker
    ```

4. **Sublime Text:**
    - Website: [Sublime Text](https://www.sublimetext.com/)
    ```bash
    brew install --cask sublime-text
    ```

5. **iTerm2:**
    - Website: [iTerm2](https://iterm2.com/)
    ```bash
    brew install --cask iterm2
    ```

6. **Sequel Ace or Sequel Pro:**
    - Sequel Pro Website: [Sequel Pro](https://www.sequelpro.com/)
    ```bash
    brew install --cask sequel-ace
    ```

7. **Bitwarden:**
    - Website: [Bitwarden](https://bitwarden.com/)
    ```bash
    brew install --cask bitwarden
    ```

   As of March 2024: If you want biometric browser integration (ie fingerprint to unlock chrome, firefox) you will need to use bitwarden from the app store.
   Version from brew/ in-website will not allow this browser integration.

9. **Anaconda:**
    - Website: [Anaconda](https://www.anaconda.com/products/distribution)
    ```bash
    brew install --cask anaconda
    ```

10. **Zoom**
    - Website: [Zoom](https://zoom.us/download)
    ```bash
    brew install --cask zoom
    ```

11. **Rectangle:** 
    ```bash
    brew install --cask rectangle
    ```

12. **Maccy:** 
    ```bash
    brew install --cask maccy
    ```


With iTerm2 / Terminal you are able to make some modifications that make life a little easier. 
Within your `~/.zshrc` file

```
plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```

you will need to run

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting
```


For ease (after brew installation):

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
sudo installer -pkg AWSCLIV2.pkg -target 
brew install pyenv
brew install poetry
brew install mysql
brew install node
brew tap databricks/tap
brew install databricks
npm install -g @aws-amplify/cli
brew install --cask visual-studio-code
brew install --cask docker
brew install --cask sublime-text
brew install --cask iterm2
brew install --cask sequel-ace
brew install --cask bitwarden
brew install --cask anaconda
brew install --cask zoom
brew install --cask rectangle
brew install --cask maccy
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting
```
