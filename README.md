<h1 align="center">
	<img
		width="500"
		alt="MCsniperPY"
		src="https://i.imgur.com/hl7h1ta.png?sanitize=true">
</h1>

<h3 align="center">
	A Fast, async, and open source Minecraft name sniper.
</h3>

<p align="center">
	<strong>
		<a href="https://mcsniperpy.github.io/">Website</a>
		•
		<a href="https://">Usage</a>
	</strong>
</p>
<p align="center">
	<a href="https://github.com/MCsniperPY/MCsniperPY">
	<img
		alt="GitHub Stars"
		src="https://img.shields.io/github/stars/MCsniperPY/MCsniperPY?color=%2370a1d2&label=Stars%20%E2%AD%90"></a>
	<a href="https://python.org/download"><img
		alt="Python Versions"
		src="https://img.shields.io/badge/Python%20Versions%20%F0%9F%90%8D-3.7%20%7C%203.8-%2370a1d2"></a>
		<a href="https://mcsniperpy.github.io/discord"><img src="https://img.shields.io/discord/734794891258757160?color=%2370a1d2&label=Discord&logo=discord&logoColor=white"></a>
</p>

<p align="center">
	<img src="https://i.imgur.com/5PUNwfR.gif" width="550">
</p>

## Table of Contents

<ul>
    <li><a href="#Installing">Installing</a></li>
    <li><a href="#Setup">Setup</a></li>
    <li><a href="#Config">Config</a></li>
    <li><a href="#Delays">Delays</a></li>
    <li><a href="#Running-the-sniper">Running the sniper</a></li>
    <li><a href="#Understanding-the-logs">Understanding the logs</a></li>
  </ul>

## Installing

You will have to have a few things installed before running the sniper. This installation guide assumes that you are on a 64bit Windows system.

First, you will need to install Python. It's recommended to use either version `3.8.5` or `3.8.6`. You must use a Python version above `3.0`. Version `3.9` is not recommended due to the issues that it causes while sniping.  

### Installing Python

Go to the following link and download Python:

`https://www.python.org/ftp/python/3.8.5/python-3.8.5-amd64.exe`

Once you have opened the installer, make sure that you check the box that adds Python to PATH. This allows your computer to recognize Python commands executed in the command prompt, which is necessary for the next steps of the tutorial. Your installer should look like this:

<img align="center" src="https://i.imgur.com/iefWNyw.png">

Run through the installer as normal, then download the McSniperPY files.

### Downloading McSniperPY

Download the following file:

`https://github.com/MCsniperPY/MCsniperPY/archive/master.zip`

Extract the folder to somewhere easily accessible, such as your desktop.

You should have a folder containing the following files:

<img src="https://i.imgur.com/pdB8Y8P.png">

If you have more files than this, don't worry; the sniper has most likely been updated since this guide was written.
If your folder doesn't have a file called `accounts.txt`, then you'll have to create one manually. 

### Installing dependencies

You now need to open a command prompt to the McSniperPY path. An easy way to do this is by opening the folder and typing `cmd` in the path:

<img src="https://i.imgur.com/qWfwXIL.png">

Your command prompt should display a line similar to this:

`C:\Users\%USERNAME%\%PATH%\MCsniperPY-master>`

If there is nothing following your Windows username, you will have to type the following command:

`cd path_to_folder`

Once you have a commant prompt open to the correct path, you should type the following command:

`py -m pip install -r requirements.txt`

If you get the following message:

`'py' is not recognized as an internal or external command, operable program or batch file.`

then you will need to reinstall Python following the guide above, make sure that you add Python to PATH (please refer to the "Installing Python" section for information on how to do so).
If you get a red error, with this message inside:

`error: Microsoft Visual C++ 14.0 is required.`

then you will need to download Microsoft Build Tools. You can do that by downloading the following program and installing Build Tools:

`https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools`

If you don't see any of these errors, then you have installed the correct dependencies and can continue with the tutorial.
If you have a problem and can't figure it out, feel free to ask for help in `#support` in the McSniperPY Discord server.

### Installing Dimension 4

Sometimes your computer's time may be out of sync. If this is the case with your computer, then all of your name snipes will be inconsistent, meaning you can't figure out your delays properly and any successful snipes that you do experience are a result of pure chance. Dimension 4 fixes this. The UNIX equivalent to this is called chrony.

Download Dimension 4 from the following link (download is at the bottom of the page):
 
`http://www.thinkman.com/dimension4/download.htm` 

Install Dimension 4, then open it.

<img src="https://i.imgur.com/sFTBS44.png">

Click the "Sync Now" button at the top right; your time should now be properly synced.

You can check if your time is synced by visiting the following website:

`https://time.is/`

## Setup

You have to provide the sniper with accounts to snipe names on; you can also edit the `config.txt` file for more advanced options if you'd like. 

### Accounts

Open the file `accounts.txt` and enter your account login information.

The proper format for login information is:

`email:password:sq1:sq2:sq3`

Sq1, 2 and 3 being the answers to the account's security questions (if they exist). The order of these is the same order that they appear in on the Minecraft website.
The security questions are optional. To add another account, simply press "Enter" to create a new line in the text file, then input the login information of your other account. Every account will follow the same login info format.

Here's an example of a valid `accounts.txt`:

```
email@gmail.com:Password1
email@hotmail.co.uk:Password2:Dogs:Cats:Llamas
```

###### Note that currently only Mojang accounts are supported.

### Config

The config file is where you can customize the sniper; it is found at `config.txt`.

You can freely modify all of these values, but please familiarize yourself with their functions before trying them out. Certain values can hinder your operation of the sniper, or even prevent it from being used at all. 

Here's what all of the current options do:


| Key | Possible Values| Explanation|
| ------------- |:-------------:| -----:|
| timing_system      | namemc | What timing system to use |
| skin      | path      |  The path to a skin to upload when a snipe is successful|
| skin_model | slim, classic      | What skin type to use when uploading |
| change_skin | true, false    | Whether the sniper should change skin on a successful snipe |
| snipe_reqs | number    | How many requests per account to send when sniping |
| auth_delay | number    | Time in milliseconds to login to accounts before the name is released |
| max_accs | number    | Maximum number of accounts to use when sniping |

Optional features:

| Key | Possible Values| Explanation|
| ------------- |:-------------:| -----:|
| custom_announce | token    | Your token for the Discord server's custom announcer |
| wh | webhook | Discord Webhook URL  |

To get a custom_announce token, join the Discord server and type `>generate` in the `#bot-commands` channel. Copy the code that you receive from the bot, then paste it into the `config.txt` file. Make sure to include the `custom_announce:` at the beginning of the code. 

## Delays

A delay is the time in milliseconds at which the sniper starts to send requests before the name drop time. If a name drops at `10:00:59` and you tell the sniper to use a delay of `1000`, the sniper will start sending the requests at `10:00:58` because 1000 milliseconds = 1 second.

Delays are useful for 2 reasons — ping and server lag.

If you have high ping (response time) to Mojang's APIs (api.minecraftservices.com, not api.mojang.com - they're seperate servers) then using a higher ping is recommended, vice versa goes for lower pings. Note that MinecraftServices is hosted in Ashburn, Virginia. You can check your ping by opening a command prompt (it does not have to be located in the MCsniperPY folder path), then typing `ping api.minecraftservices.com` and pressing Enter. The resulting number that the computer gives you should be added to your custom delay to ensure that your ping doesn't impede the sniping process. 

If a lot of people are going for a username (you can usually determine this by the number of views it has on NameMC), then Mojang's servers can lag. It's generally advised to use a higher delay when going for a name with high views.

In most cases, other people's delays won't work on your machine. Delays can depend on many things, including ping, network routes and even CPU speed, so your delay is generally unique to your particular situation. 

A good way to find a delay that works for you is to attempt to snipe usernames with a delay of `400`, then adjusting the delay based on the timestamp you receieve. If the snipe is early, your delay is too high.

If you need help with your delays, and have followed the suggested method above, then you can ask for help in the `#support` channel in McSniperPY's Discord server.

## Running the sniper

To run the sniper, open a command prompt window where McSniperPY is located.

You can do that like so:

<img src="https://i.imgur.com/qWfwXIL.png">


Once the window is open, type the following command:

`py snipe.py`

Assuming nothing went wrong, the sniper should now be running;

<img src="https://i.imgur.com/3YZ0pP3.png">

You can now follow the onscreen instructions.

## Understanding the logs

When you attempt to snipe a name, you are given information about the requests that McSniperPY sends to Mojang's API. This information is in the following format: 

`[fail/success] [http status code] @ [timestamp]`

The timestamp is the time that you sent the request to Mojang's servers.

### HTTP Status Codes

When the sniper sends requests to a server, it returns a HTTP Status Code. Mojang's API returns a status code based on what we requested; in terms of name sniping, the status codes and their meanings can be seen below:

| Status Code | Meaning|
| ----------- | ----------- |
| 200 | Sniped name successfully |
| 403 | Name is unavailable, failed to snipe name |
| 429 | Account or IP is rate limited |
| 500 | Minecraft API issue |

A 429 status code can be avoided by reducing the number of snipe requests sent per account. You can do this by editing the `snipe_requests` value in the `config.txt` file. To completely eliminate 429s, lower your snipe requests to 3. This can drastically decrease your odds of successfully sniping a name, however, so only do this if other, higher values have failed. It's recommended to start with a base value of 6 for your snipe requests and adjust it from there if 429s still persist. 



