# WSL setup

```bash
git clone https://github.com/tsuneto-lab/wsl-setup.git
```

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

ansible-playbook -K nvidia-docker.yml
docker run --rm --gpus all nvidia/cuda:11.6.2-base-ubuntu20.04 nvidia-smi
# docker run --rm --gpus all nvidia/cuda:11.7.1-base-ubuntu22.04 nvidia-smi
```

## Available base images

A note for my convenience.
search tags on [dockerhub](https://hub.docker.com/r/nvidia/cuda/tags) by below keywords.

```
nvidia/cuda
:12.0.0 11.8.0 11.7.1 11.6.2 11.5.2 11.4.3 11.3.1 11.2.2 11.1.1 11.0.3 10.2 9.2
[-cudnn8]
-devel runtime base
-ubuntu22.04 ubuntu20.04 centos7 ubi8 ubi7 rockylinux8
```