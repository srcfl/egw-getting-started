# egw-getting-started

This is a step-by-step guide on how to get started with your energy gateway. 

![Alt text](/images/egw500.png)

Step 0 and 1 are only needed if your gateway SD is damaged and you need to flash the firmware again. Skip step 0 and 1 if you just received your gateway and want to get started with the configuration.

## Step 0 - Download the firmware
If your SD card is damaged or you want to flash the firmware again, you can download the firmware and flash it to your SD card. Below are the different firmwares and their corresponding gateway models:

| Hardware | Firmware |
| --- | --- |
| Srcful Energy Gateway | [srcful-egw.img](https://drive.google.com/file/d/1Oa-XKZwZGY7xrMGAAt81Qn4FMCvqX9Rv/view?usp=drive_link) |
| RAK hotspot v2 | [rak-srcful-egw.img](https://drive.google.com/file/d/1wkd7ED6-rkmPFGFnaIz0RuI1pTabiFMJ/view?usp=drive_link) |
| --- | --- |


## Step 1 - Flashing the firmware
The firmware can be flashed using, for example, Balena Etcher. Download and install Balena Etcher from [here](https://www.balena.io/etcher/). Connect the SD card to your computer and flash the firmware using Balena Etcher.

## Step 2 - Starting & pairing
Make sure the gateway is connected to the internet with an Ethernet cable (just for the initial setup) and power on the gateway. Wait ~10 minutes for the system to start up and fetch the latest firmware.

Then remove the Ethernet cable if you want to connect to WiFi instead and visit https://start.srcful.io/ to get started with the gateway configuration.


![Alt text](https://github.com/srcfl/egw-getting-started/raw/main/images/image.png)

Once your device is paired with the gateway, you should see an output in the white terminal section indicating that similar to the one below. 

![Alt text](https://github.com/srcfl/egw-getting-started/raw/main/images/image-1.png)

The `internet connection` status under [Step 2](#step-2) should also say `Connected` or `Not connected`. 

Note: If the `internet connection` is `Unknown`, then there might be a bluetooth pairing issue. In that case, ty the pairing process again. Changing the browser might sometimes help. IPhone will not work for this, but MAC will (and pc + android).
More info on this soon...

Wait ~1 minute before moving on to the next step. 

## Step 3 - Network configuration
This is a straight forward step. If you with to connect your enery gateway over ethernet, please skip this step. 

![Alt text](https://github.com/srcfl/egw-getting-started/raw/main/images/image-2.png)

Note: The `internet connection` should say `Connected` when connected over ethernet. 

This may take a couple of minutes, so please wait for the status message to update before moving on to the next step. 

## Step 4 - Solana wallet setup
To participate in token distribution, you need to have a solana wallet.

This is needed for you to receive your `SRC-tokens` and see your device on the explorer. Add your wallet address and click `Set Wallet Config`.

![Alt text](https://github.com/srcfl/egw-getting-started/raw/main/images/image-3.png)

Wait ~1 minute before moving on to the next step. 

## Step 5 - Inverter configuration
Finally, enter the neccessary inverter details. The Gateway needs an `IP-address`, `port`, `modbus device address` and the `type` of the inverter. 

We will, in the near future, have an option to scan the local network for inverters. But for now, users need to know the IP-address of their inverter.

![Alt text](https://github.com/srcfl/egw-getting-started/raw/main/images/image-4.png)

Note: Currently, there is no way of knowing if the gateway is successfully reading and sending inverter data.. To confirm, please reach out to @damo030 on TG.

Note: If running our [inverter-simulator](https://github.com/srcfl/inverter-simulator), then the server will start outputting data frequently. This is a sign that the gateway is successfully reading and sending "inverter" data.

## Step 6 - Add your gateway to the explorer
More info on this soon...