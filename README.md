# ansible_home_assistant_pi      Cancel changes


### Run the following commands:

```
sudo apt-get update && sudo apt-get upgrade -y && sudo sudo apt install ansible git -y
```

```
sudo reboot
```

```
git clone https://github.com/BoasHoeven/ansible_home_assistant_pi.git
```

```
cd ansible_home_assistant_pi
```

```
ansible-playbook main.yml
```

### Contains the following docker containers:

Portainer can be enabled via config option

Pi-Hole can be enabled via config option

Home Assistant

To also create a Pi-Hole container in docker you can edit the config.yml file.
<br>
> **If running locally on the Pi**: You may encounter an error like "Error while fetching server API version". If you do, please either reboot or log out and log back in, then run the playbook again.
