# kimono koans' Github PPA

This is a PPA for a few packages I build for myself.  The packages contained within are built using Ubuntu 20.04 because that is the oldest non-deprecated version of Ubuntu available for a GitHub action workflow, and these packages seem to work fine with Ubuntu 22.04.

## Caveats

No support is offered by me for this PPA, for `apt`, for Ubuntu, or for any of the instructions offered below.  It somehow works on my system!

You should *never* ask me when a package is going to be available, or if I can build for your very particular system.  Again, this PPA is only for me.

Of course, you're always free to build from my sources and start your own PPA at your leisure.  There are many wonderful blog entries about how to do so.  You're encouraged to [read one](https://assafmo.github.io/2019/05/02/ppa-repo-hosted-on-github.html).

If you'd like more information regarding [httm](https://github.com/kimono-koans/httm) and [dano](https://github.com/kimono-koans/dano) and [two_percent](https://github.com/kimono-koans/two_percent), please visit their respective repos.

Good luck!

## Instructions

```bash
# add my public key to list of trusted keys
curl -s --compressed https://raw.githubusercontent.com/kimono-koans/ppa/main/KEY.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/kimono-koans.gpg >/dev/null
# add package list to repos to search
sudo curl -s --compressed -o /etc/apt/sources.list.d/kimono-koans.list "https://raw.githubusercontent.com/kimono-koans/ppa/main/kimono-koans.list"
# update apt
sudo apt update
# install httm if you want
sudo apt install httm
# install dano if you want
sudo apt install dano
# install dano if you want
sudo apt install two_percent
```
