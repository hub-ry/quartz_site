The reason I started this project was to learn, but also because using third party products such as Replit was very annoying (specifically at their free tiers).

This Linux PC will stay on 24/7, in my university dorm.
#### Hardware

Model : HP Slimline Desktop PC 270-p0xx
Processor : Intel Core i3- 7100 x 4
Memory : 16 gigs , i added an extra 8 gigs of ram
Graphics : Intel HD Graphics 630 (integrated)
Disk Capacity : 1.0 TB

This was a pc I found in my family's attic. I only added extra ram because I had some lying around. 

I also have a nicer gaming pc that runs windows and a Mac with MacOS, so its fair to say this project is rounding out my OS knowledge.

#### Downloading Linux

I chose to use Ubuntu. Maybe I'll explore other Distros one day, but I plan to use the combination of [open-ssh](https://www.openssh.org/),  [tailscale](https://tailscale.com/) and [flask](https://flask.palletsprojects.com/en/stable/) for personal project such as creating my own server.

I watched a YouTube video for the install. I couldn't remember which one but it just used USB stick and [Etcher](https://etcher.balena.io/)

#### Config

I have a [NVIM](https://neovim.io/) setup, I use [quartz](https://quartz.jzhao.xyz/), I don't care to do more config for something I'm using as a server. That's part of the reason i chose Ubuntu (Mint was close second).


#### Tailscale (VPN Tunneling)

One of the biggest issues I ran into at the start of making personal projects, was needing to be on the same network for flask methods to work. This was necessary because 
1. I want to access project when I'm outside the network
2. My server will be on university wifi, so there is no port forwarding workaround I could use.

Tailscale is one of the smoothest, easiest programs I have ever used, 10/10 btw.


#### open-ssh server

I think this may be Ubuntu specific, at least to some extent. 

Install on Linux
```bash
sudo apt install openssh-server

sudo systemctl start ssh sudo systemctl enable ssh

bash
sudo systemctl status ssh

```


##### Ssh Config [[ssh-config]]

before any config:

```
ssh username@ip_of_linux_server
password: __

```

to make the name shorter

you do this on your local machine (locally)

```
vim ~/.ssh/config



Host hub (or whatever you want to type)
	HostName ip
    User linux-username
```


now it will be 

```
ssh hub
password: __
```

Now that password is still annoying, especially if there is 2fa.

##### SSH Keys

*non-ssh'd on your non server machine*

```
ssh-keygen -t ed25519

ssh-copy-id hub

password: __

ssh hub
```

if you already have a generated key (specifically ed25519) you can do 

```
ssh-copy-id hub
password: __
```

Now it works.

