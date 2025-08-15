# Semaphore Trusted Setup Ceremony

Semaphore is a zero-knowledge protocol for anonymous signaling on Ethereum, enabling users to prove membership in a group and broadcast signals. Such as votes, endorsements, or messages. Without revealing their identity.

<img width="1118" height="521" alt="image" src="https://github.com/user-attachments/assets/2a7e6b40-cfa5-4de8-8d19-9cb1b64bf563" />

## Contribute
You can contribute to the ceremony using either a web browser or the command-line interface (CLI).

- Web-browser: Simply connect your github in ceremoy.pse.dev, press on Contribute and wait for your contribution to finish.
- CLI: Follow the below guide to install and participate the ceremony in a terminal using command-line. This method is way more stable than the web version.

--------------------------- 
## Requirements
## Operating System
You need one of these to join the ceremony:

- Linux
- MacOS system
- WSL (linux) on Windows
- VPS with Ubuntu OS

## GitHub Account

Your GitHub account must meet the following criteria:

At least a month old.
At least one public repository.
At least following 5 GitHub accounts and have at least 1 follower.
Must allow the ceremony tools to read and write GitHub Gists on your account.

Internet Connection
You need a stable internet connection on your local system or a VPS to stay in the ceremony queue for hours, waiting for your turn.

-----------------------------------------
## Install Dependecies

## Install Dependecies
1. Packages:
```
sudo apt-get update && sudo apt-get upgrade -y

sudo apt install curl screen iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev ca-certificates  -y
```

2. Install NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source .bashrc
```

3. Install Node.js 18
```bash
nvm install 18 
nvm use 18
```
```
source ~/.bashrc
```

---

## Install Ceremony
### Step 1. Create a directory in your home folder to run the ceremony from:
```
mkdir ~/trusted-setup && cd ~/trusted-setup
```

### Step 2: Install CLI:
```
npm install -g @p0tion/phase2cli
```

### Step 3: Authenticate with GitHub:
To contribute to the ceremony, you’ll need a legit GitHub account.

Run this command in your terminal:
```
phase2cli auth
```
* This will prompt you to open a browser and visit [https://github.com/login/device](https://github.com/login/device)
* Copy the provided auth code in terminal and paste in the auth page . Click "Authorize" to continue.

---

## Contribute Ceremony
### Open a screen
Open a screen so the ceremony keeps going in the background—might take hours before it’s your turn.
* Screen is useful for VPS, not WSL. If you close the terminal in WSL, your screen session is killed
```
screen -S semaphore
```

### Contribute to the ceremony
```
phase2cli contribute -c semaphore-binary-merkle-root-fix
```
* You can either hit enter for randomly, or pick manually and type any letter or number yourself.

<img width="689" height="302" alt="image" src="https://github.com/user-attachments/assets/8830a33c-8e97-4cd1-8b6e-9ca0d7312dd7" />

### Screen commands
* Minimize screen: `Ctrl`+`A`+`D`
* Return to screen: `screen -r semaphore`
* Kill ceremony when inside screen: `Ctrl`+`C`
* Kill screen when inside screen: `Ctrl`+`D`
* Kill screen when outside screen: `screen -XS semaphore quit`
* screens list: `screen -ls`

---

## Notes:
* Contributing may take some time, depending on the number of circuits (**32 in this run**) and the queue of contributors.
* If your connection is interrupted or an error occurs, simply re-run the same command — it will pick up from where it left off.

### After completing your contribution, you will be invited to share a message on X or your preferred social platform! 🎉

---

## Cleanup & Logout
After completing your contribution to the ceremony, it’s recommended to clean up your local files and revoke GitHub authorization for security:
```
phase2cli clean
```
```
phase2cli logout
```
Delete the ceremony folder too if you don’t need it:
```
rm -rf ~/trusted-setup
```
