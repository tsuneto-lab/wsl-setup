# WSL setup

## prerequisite

```bash
sudo apt update
sudo apt upgrade

sudo apt-get install python3-pip
python3 -m pip install --user ansible

source ~/.profile
```

## play

```bash
ansible-playbook -K main.yml
# restart wsl manually from windows
# e.g. wsl -t Ubuntu-20.04

docker run hello-world

ansible-playbook -K docker-cuda.yml
docker run --rm --gpus all nvidia/cuda:11.6.2-base-ubuntu20.04 nvidia-smi
```