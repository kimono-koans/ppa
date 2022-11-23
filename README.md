# kimono koans' Github PPA

This is a PPA for a few packages I build for myself.  

No support is offered for this PPA, for `apt`, or for the instructions below.

If you'd like more information about [httm](https://github.com/kimono-koans/httm) and [dano](https://github.com/kimono-koans/dano), please visit their respective repos.

```bash
# add my public key to list of trusted keys
curl -s --compressed https://raw.githubusercontent.com/kimono-koans/ppa/main/KEY.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/kimono-koans.gpg >/dev/null
# add package list to repos to search
sudo curl -s --compressed -o /etc/apt/sources.list.d/kimono-koans.list "https://raw.githubusercontent.com/kimono-koans/ppa/main/kimono-koans.list"
# update apt
sudo apt update
# install httm if you want
sudo apt install httm
# install dano if want
sudo apt install dano
```
