## Set up filesystem
 * pogramming
 * graphic design
 * web design
## Install dev software
 * Windows Subsystem for Linux `wsl --install`
 * [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/#install-winget)
 *  [PowerShell 7](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.3)
 	- `winget search Microsoft.PowerShell`
 	- `winget install --id Microsoft.Powershell --source winget`
 * compilers?
 * SSH `ssh-keygen`
 * [Choclatey](https://chocolatey.org/install) - optional, if not using winget
 * [Git](https://git-scm.com/download/win)
	 - `git config --global user.name "Steve Baney"`
	 - `git config --global user.email "steve.baney@gmail.com"`
 * [Git CLI](https://github.com/cli/cli#installation)
 * [Node](https://nodejs.org/en/download/package-manager/#windows-1)
 * [Ubuntu Node](https://github.com/nodesource/distributions#debinstall)
	 - `curl -fsSL https://deb.nodesource.com/setup_19.x | sudo -E bash - &&\`
	 - `sudo apt-get install -y nodejs`
 * VSCode Extensions
	 - Docker
	 - WSL
         - VSCodeVIM
	 - GitHub Pull Requests and Issues
	 - GitHub Copilot
	 - [Live Server](https://github.com/ritwickdey/vscode-live-server)
	 - Prettier
	 - ES7+ React/Redux/React-Native Snippets
	 - JavaScript and TypeScript Nightly
	 - Tailwind CSS IntelliSense
 * HTTRack
 * [Docker Desktop](https://www.docker.com/products/docker-desktop/)
 * zsh / oh-my-zsh
	 - `sudo apt install zsh`
	 - [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
 * [mySQL Driver](https://www.npmjs.com/search?q=mysql)
	 - `npm install mysql2`
 * [Gatsby](https://www.gatsbyjs.com/docs/tutorial/part-0/#gatsby-cli) - `npm install -g gatsby-cli`
 * [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/#windows-stable) - `npm install --global yarn`

## Config dev environment
 * [WSL development environment](https://learn.microsoft.com/en-us/windows/wsl/setup/environment)_
 * VSCode
	 - Solarized
	 - Format on Save - `settings.json` - `"editor.formatOnSave": true`
 * [Set Up SSH Keys in WSL](https://devblogs.microsoft.com/commandline/sharing-ssh-keys-between-windows-and-wsl-2/)
	 - `cp -r /mnt/c/Users/steve/.ssh ~/.ssh`
	 - `chmod 600 ~/.ssh/id_rsa`
	 - `sudo apt install keychain`
	 - `vim ~/.bashrc` add `eval ``keychain --eval --agents ssh id_rsa`
 * Docker Desktop
	 - Settings > Resources > WSL Integration (should be enabled by default)
	 - `Enable integration with additional distros` - Enable for Ubuntu
 * Windows Terminal
	 - Settings > Profiles > Ubuntu > Starting Directory > `//wsl$/Ubuntu/home/steve`
 * [Auto-launching ssh-agent on Git for Windows](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases)
 * Generate and add secondary SSH key 
 	- `ssh-keygen -t ed25519 -C "sbaneydesign@gmail.com"`
 	- `eval `keychain --eval ~/.ssh/id_ed25519``
 * [Remove Cached GitHub Credentials](https://stackoverflow.com/questions/47465644/github-remote-permission-denied) (for multiple accounts) - Control Panel\User Accounts\Credential Manager
