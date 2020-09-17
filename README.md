# NFC EEPROM usage example for X-NUCLEO-NFC04A1

Demonstration of possible usage of the NFC EEPROM class. 

The application will write an URL to the EEPROM of the NFC tag on your board. This will be able to be read by any NFC device capable of reading NFC tags.

The example needs to supply a driver for the EEPROM. The `ST25DV` EEPROM driver is provided for the `NUCLEO_F401RE` target. You may wish to update the configuration if you're using a different target.

# Running the application

## Requirements

Verification of the sample application can be seen on any smartphone with a NFC reader. After running you will be able to read the tag with a NFC tag reader application running on the smartphone.

Information about activity is also printed on the serial interface. See the [official documentation website](https://os.mbed.com/docs/mbed-os/v5.15/tutorials/serial-comm.html#using-terminal-applications) for more informartion about using serial terminals.

As mentioned above, this example is known to work on the `NUCLEO_F401RE` target which uses the [`ST25DV`](./source/target/TARGET_ST25DV) driver.

If your are not using a `NUCLEO_F401RE` you should indicate in the application configuration file ([`mbed_app.json`](./mbed_app.json)) which driver should be selected by the build system as follows:

```json
    "<TARGET_NAME>": {
        "target.extra_labels_add": ["ST25DV"]
    }
```
