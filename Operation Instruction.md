# Operation Instruction

## Hardware Connection

Connect the Bluetooth module and the development board with the Dupont wire as follows.

| Bluetooth module pin | STM32 Development board pin |
| :------------------: | :-------------------------: |
|         VCC          |            3.3V             |
|         GND          |             GND             |
|         TXD          |             PA3             |
|         RXD          |             PA2             |
|         KEY-         |              -              |
|        STATE         |             PA4             |

Connect the development board to the COMPUTER's USB port with a USB to serial cable.

## Software operation

**Users can input "$"+"instruction" to configure the Bluetooth model.**

Instruction set：

```
$search_devices: Search surrounding devices
$set_role: Set up master or slave
$set_bind_address: Set the default connection address
$set_pswd: Set device's password
$set_name: Set device's name
$link: Pair device with the specified address
$get_addr: Get device's address
$get_name: Get device's name
$get_pswd: Get device's password
```

**Note**: Needs to press the button on the module continuously when sending instructions to the Bluetooth module.

**SSCOM GUI**

<img src="C:\Users\MACHENIKE\Desktop\嵌入式\dd.PNG" alt="dd" style="zoom:67%;" />

Operation order：

```
$set_role=MASTER
$set_pswd=1234
$set_bind_address=xxxxx
$link
```

After connecting with other device, users can send anything which is shorter than 27 bytes without "$" as front.

