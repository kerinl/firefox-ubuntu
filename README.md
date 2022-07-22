# Replace snap version of Firefox on Ubuntu
## Step by step guide to replace snap version of Firefox, that ships by default on Ubuntu.

1)
`sudo snap remove --purge firefox`

2)
`sudo add-apt-repository ppa:mozillateam/ppa`

3)
`sudo apt install --target-release 'o=LP-PPA-mozillateam' firefox`

4)
`sudo nano /etc/apt/preferences.d/mozillateamppa`

5)
#### Insert these lines in the file above:
`Package: firefox*`<br />
`Pin: release o=LP-PPA-mozillateam`<br />
`Pin-Priority: 501`

6)
`sudo apt update`
