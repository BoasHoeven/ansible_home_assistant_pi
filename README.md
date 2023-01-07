# ansible_home_assistant_pi

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

To also create a Pi-Hole container in docker you can edit the config.yml file.
<br>
You maybe have to run the ansible playbook twice because the first time the 'pi' user may not have been added yet.
