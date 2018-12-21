# Custom Component For Home Assistant
## Ubiquiti Unifi Access Switch

This platform allows you to block/unblock devices based upon the MAC address.

To use this switch in your installation, add the following to your `configuration.yaml` file:

```
switch:
  - platform: unifi_access_switch
    host: unifi.domain.name
    username: username
    password: password
    name: device_name
    mac_address: 00:00:00:00:00:00
```

#### CONFIGURATION VARIABLES
**host** (Required): The hostname or IP address of your controller
**username** (Required): A user on the controller
**password** (Required): The password for the user account
**mac_address** (Required): The MAC address of the network attached device to be blocked/unblocked
**name** (Optional): The device name (Default value: DEFAULT_NAME)
**verify_ssl** (Optional): Whether to do strict validation on SSL certifications of the Unifi Controller.  This can be true/false. (Default value: True)

#### INSTALLATION
Place `unifi_access_switch.py` in `your_config_directory/custom_components/switch/`
Validate configuration with UI
Restart Home Assistant to load component
