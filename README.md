<p align="center">
<img src="https://github.com/Bikoil/Magicord/blob/main/Magicord.png" width="100px">
</p>
<h1 align="center">
  Magicord
</h1>
<div align="center">
<em> An Open Source Discord Bot Written in TypeScript </em>
</div>
  
<p align="center">
<img src="https://img.shields.io/badge/Discord.js-Bot-Bot?style=for-the-badge"> 
<img src="https://img.shields.io/github/commit-activity/m/Bikoil/Magicord?style=for-the-badge"> 
<img src="https://img.shields.io/badge/WorkInProgress-JS?style=for-the-badge">

</p>






***
***



# What is Magicord?
- Magicord used to be a bot primarily hosted on [Botghost](https://botghost.com) but since it was unreliable and had limitations, I decided to move it to [Discord.js](https://discord.js.org) and [Discordx](https://discordx.js.org/), everything is still being moved so not everything has been added here.
# Features
- Modern reaction roles
- Setup applications as an alternative to google forms
- Safety system against raids
- Configuration to your liking
- Edit the bot's code to your liking! (Need js knowledge)
- Silly commands (cuz why not)

__NOTE THAT MOST OF THESE FEATURES HAVE NOT BEEN IMPLEMENTED YET__

[![Get Magicord](https://raw.githubusercontent.com/Bikoil/Magicord/main/AddMagicord.png)](https://discord.com/api/oauth2/authorize?client_id=1138504372817506344&permissions=8&scope=bot)
    
# Commands
- Here is the list of current commands of magicord!


| Command      | File                        | Description                                                             | Permissions       |
|--------------|-----------------------------|-------------------------------------------------------------------------|-------------------|
| Ban          | `commands/ban.ts`            | Bans a member from the server                                            | `BAN_MEMBERS`     |
| Echo         | `commands/echo.ts`           | Makes the bot say anything you want it to say                            | `ADMINISTRATOR`   |
| Embed Message | `commands/embedmsg.ts`      | Makes the bot send an embed message                                      | `ADMINISTRATOR`   |
| Kick         | `commands/kick.ts`           | Kicks a member from the server                                           | `KICK_MEMBERS`    |
| Mute         | `commands/mute.ts`           | Mutes a member by giving the member MUTED role and prevents them from talking anywhere | `TIMEOUT_MEMBERS` |
| Unmute       | `commands/unmute.ts`         | Unmutes a user by removing muted role from them                          | `TIMEOUT_MEMBERS` |
| Ping Check   | `commands/pingcheck.ts`      | Checks if the bot is online and gives RAM and CPU usage                   | `@everyone`       |
| Uptime       | `commands/uptime.ts`         | Checks how the bot has been active for and when the latest change of the source code was done | `@everyone`       |
| User         | `commands/user.ts`           | Lists information about the user                                         | `@everyone`       |
| Stats        | `commands/stats.ts`          | Checks stats about the bot and the system that the bot is being hosted on | `@everyone`       |


***
***


# How to setup the bot
> [!IMPORTANT]  
> Before setting up the bot, you must have at least some JavaScript skill or are familiar with the language, do not open issues on learning JavaScript/TypeScript or "where do I begin from", please look at [Discord.js guide](https://discordjs.guide) and [Discordx guide](https://discordx.js.org/docs/discordx/getting-started/) for more information about Discord TypeScript, you may also learn JavaScript at the [JavaScript website](https://www.javascript.com/) and TypeScript at [TypeScript website](https://www.typescriptlang.org/docs/), Also, you may need to have some knowledge about the terminal and how to use it including bash and other shells.
> Please also Keep in mind this bot is not complete at all, and is still being worked on.


- Firstly, you will have to clone this repository using git or gh cli, if you plan on using git for long term purpose (as in a project) then you may want to keep using git after cloning.

- *"How do i clone a repository?"*
 - You have 2 options to clone the repository, either by using git as listed ealier or by forking the repository then using github desktop, i recommend using git, but if you aren't experienced with terminals and such, you may use github desktop.

 ## Cloning the repository using git cli

- Run the following command in git bash or in terminal (if you are using windows), this guide should work perfectly with linux systems and unix systems (like MacOS and FreeBSD)

You may not have git installed by default, so, install it depending on the OS

Another thing you will have to install is npm (Node Package Manager) for JS, or node

### Windows

to install git on windows you can either run this in command prompt

```bash
winget install --id Git.Git -e --source winget 
# to install npm
winget install -e --id OpenJS.NodeJS
```

or by installing it from [The official git website](https://git-scm.com/)

### Linux Distros

- **Debian**
```bash
sudo apt install git
# to install npm
sudo apt install npm
```
- **Arch Linux**
```bash
sudo pacman -S git
# to install npm
sudo pacman -S npm
```
- **Fedora**
```bash
sudo dnf install git
# to install npm
sudo dnf install git nodejs 
```

If you are using any other distro, you should be able to do it on your own

### MacOS/FreeBSD

- **MacOS**

Firstly, install [Homebrew](https://brew.sh/) if you haven't yet
```bash
brew install git
# to install npm
brew install node
```

- **FreeBSD**
```bash
sudo pkg install git
# to install npm
sudo pkg install node
```
> [!IMPORTANT]
> This part of the guide needs YOUR Help in adjusting since most of this OS's were not experimented when installing the packages, if there is any mistake within this part, please open a pull request/issue correcting it, the tested OS's are
> - Arch Linux
> - Debian
> - Fedora
>
>
> I would heavily appreciate your corrections on this part, thank you


***

With git installed now its time to clone the repository

```bash
git clone https://github.com/Bikoil/Magicord
```

If you forked the repository, then you should do the following instead

```bash
git clone https://github.com/<YourUsername>/<YourMagicordForkName>
```
> WARNING: THIS PART BELOW IS NOT RECOMMENDED.
_If you want to use the latest version of Magicord with the latest changes_

```bash
git clone -b Magicord-RollRelease https://github.com/Bikoil/Magicord
```
> ONLY DO THIS IF YOU KNOW WHAT YOU ARE DOING. THIS WILL MOST LIKELY CAUSE MANY ERRORS OR STRAIGHT UP NOT WORK


Now, your bot repository is setup in your device, you are missing 2 more steps before the bot is setup

# Setting the bot up with your bot token

> [!IMPORTANT]
> NEVER ever give your bot token to absolutely ANYONE, giving your bot token to anyone or leaking it can cause **catostrophic events** to your bot and the servers it is inside, leaking it essentially gives the person access to the bot and do absolutely anything you want, this is fully YOUR responsibility and you should take care of it.

Now, you can either keep going with the terminal to setup everything if you are used to the terminal, you will have to make a file in the bot folder

- Go to your bot folder
- Make a file named `config.json`
> [!IMPORTANT]
> If you are hosting your bot on a public git platform (like github or gitlab) then DO NOT delete the `.gitignore` file as it prevents your token from being leaked and stops config.json from appearing on the public git repository

- Copy this to the `config.json`
```json
{
	"token": "<YourBotToken>",
	"clientId": "YourBot'sClientID",
	"guildId": "YourServerID"
}
```
> [!IMPORTANT]
> This step may be changed soon in the future.

Then run the following
- **Windows**
```cmd
// For cmd
set BOT_TOKEN=YourBotToken
// For powershell
$env:BOT_TOKEN="YourBotToken"
```

- **Linux/BSD/MacOS/GitBash**
```sh
export BOT_TOKEN=YourBotToken
```
After this, you are all set! you just need to do the following to run the ot and make it online

- Go to your terminal/command prompt
- change directory to the bot folder
```bash
cd <TheBotFolderName>
```

- You will need to install all the dependencies
```bash
npm install discord.js  discordx os fs typescript date-fns-tz --save-dev @types/fs-extra
```

- And finally...
```bash
npm run build && npm run start
```

And viola! your bot is online, now you can go ahead and customize it all you want

# Running through Docker and Kubernetes
> Soon...


*Development Team: !!Cords!! - Currently not public.*
