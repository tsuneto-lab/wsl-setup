# WSL setup

## prerequisite

```bash
# fix date
sudo apt install ntpdate
sudo ntpdate ntp.nict.jp

sudo apt-get install python3-pip
python3 -m pip install --user ansible

source ~/.profile
```

## play

```bash
ansible-playbook -K main.yml
```