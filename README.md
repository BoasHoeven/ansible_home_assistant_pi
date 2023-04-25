# Ansible Home Assistant Pi Setup


## Prerequisites

```
sudo apt-get update && sudo apt-get upgrade -y && sudo apt install ansible git -y
```

```
sudo reboot
```

## Clone the Repository

```
git clone https://github.com/BoasHoeven/ansible_home_assistant_pi.git
```

```
cd ansible_home_assistant_pi
```

## Configure Ansible Vault

```
touch vault.yml
```


```
ansible-vault encrypt vault.yml
```


```
ansible-vault edit vault.yml
```

Add the following content to the vault.yml file:

```
vault_mosquitto_password: "your-mosquitto-password"
vault_pihole_password: "your-pihole-password"
```

## Install Required Collections

```
ansible-galaxy collection install -r requirements.yml
```

## Run the Ansible Playbook

```
ansible-playbook main.yml --ask-vault-pass
```

## Installed Docker Containers

The playbook installs the following Docker containers:

Home Assistant

Mosquitto

Zigbee2mqtt

Portainer (Disabled)

Pi-Hole (Disabled)

Tesla Custom Integration (Disabled)

> **If running locally on the Pi**: You may encounter an error like "Error while fetching server API version". If you do, please either reboot or log out and log back in, then run the playbook again.
