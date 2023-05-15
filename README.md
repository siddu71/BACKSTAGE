# BACKSTAGE_INSTALLATION

```
#!/bin/bash
# install build_essentials

sudo apt update
sudo apt install build-essential

# Download and install nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

# Set up NVM environment variables
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

# Install and use node v18.16.0
nvm install 18.16.0
nvm use 18.16.0

# Install yarn globally
npm install --global yarn

# Check the yarn version
yarn --version

#  Create the backstage APP

npx @backstage/create-app@latest -y 
