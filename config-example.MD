## Configurations
The configuration parameters to enable your devices would need to be added to `platforms` section of the Homebridge configuration file. Examples of device configs can be found on the [Supported Device Types](https://github.com/iRayanKhan/homebridge-tuya/wiki/Supported-Device-Types) page. Check out the [Common Problems](https://github.com/iRayanKhan/homebridge-tuya/wiki/Common-Problems) page for solutions or raise an issue if you face problems.

## Adding one device:


```json5
{
    "platforms": [{
            "platform": "Tuya",
            "devices": [
 
                {
                    "name": "Kitchen Light",
                    "type": "SimpleLight",
                    "manufacturer": "CanBeAnything",
                    "model": "CanAlsoBeAnything",
                    "id": "011233455677899abbcd",
                    "key": "0123456789abcdef"
                }
             ]
        }
   ]
   
}
```
## Adding two or more devices:

```json5
{
    "platforms": [{
            "platform": "Tuya",
            "devices": [
 
                {
                    "name": "Kitchen Light",
                    "type": "SimpleLight",
                    "manufacturer": "CanBeAnything",
                    "model": "CanAlsoBeAnything",
                    "id": "011233455677899abbcd",
                    "key": "0123456789abcdef"
                },
                
                {
                    "name": "Office Light",
                    "type": "SimpleLight",
                    "manufacturer": "CanBeAnything",
                    "model": "CanAlsoBeAnything",
                    "id": "011233455677899abbcd",
                    "key": "0123456789abcdef"
                }
             ]
        }
   ]
   
}


#### Parameters
* `name` (required) is anything you'd like to use to identify this device. You can always change the name from within the Home app.
* `type` (required) is a case-insensitive identifier that lets the plugin know how to handle your device. Find your device `type` on the [Supported Device Type List](https://github.com/iRayanKhan/homebridge-tuya/wiki/Supported-Device-Types) page.
* `manufacturer` and `model` are anything you like; the purpose of them is to help you identify the device.
* `id` (required) and `key` (required) are parameters for your device. If you don't have them, follow the steps found on the [Setup Instructions](https://github.com/iRayanKhan/homebridge-tuya/wiki/Setup) page.
* `ip` needs to be added **_only_** if you face discovery issues. See [Common Problems](https://github.com/iRayanKhan/homebridge-tuya/wiki/Common-Problems) for more details.   

> To find out which `id` belongs to which device, open the Tuya Smart app and check the `Device Information` by tapping the configuration icon of your devices; it is almost always a tiny icon on the top-right.
