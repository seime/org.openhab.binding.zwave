---
layout: documentation
title: Soft Remote  - ZWave
---

{% include base.html %}

# Soft Remote Remote Control
This describes the Z-Wave device *Soft Remote *, manufactured by *[ID-RF](http://www.nodon.fr/)* with the thing type UID of ```nodon_softremote_00_000```.

The device is in the category of *Remote Control*, defining Any portable or hand-held device that controls the status of something, e.g. remote control, keyfob etc..

![Soft Remote  product image](https://www.cd-jackson.com/zwave_device_uploads/250/250_default.png)


The Soft Remote  does not permanently listen for messages sent from the controller - it will periodically wake up automatically to check if the controller has messages to send, but will sleep most of the time to conserve battery life. Refer to the *Wakeup Information* section below for further information.

## Overview

The NodOn® Soft Remote controls any compatible receivers Z-Wave® or Z-Wave Plus®, such as the Smart Plug NodOn®. It can address, directly, up to 4 groups of 8 devices and sent up to 16 different scenes to a Home Automation Gateway. This controller can operate on its own (“Standalone” Mode) or as gateway’s assistant (“Gateway” Mode). The product integrates a LED, which give an intuitive feedback for each operation you perform.

### Inclusion Information

  1. Simultaneously push on I and P, during 1sec. The LED glows in pink to confirm the selection
  2. Push on I, within 10 seconds. The LED blinks in pink to confirm your choice The LED blinks in green to confirm the procedure

### Exclusion Information

  1. Simultaneously push on I and P, during 1sec. The LED glows in pink to confirm the selection
  2. Push on I, within 10 seconds. The LED blinks in pink to confirm your choice The LED blinks in green to confirm the procedure

### Wakeup Information

The Soft Remote  does not permanently listen for messages sent from the controller - it will periodically wake up automatically to check if the controller has messages to send, but will sleep most of the time to conserve battery life. The wakeup period can be configured in the user interface - it is advisable not to make this too short as it will impact battery life - a reasonable compromise is 1 hour.

The wakeup period does not impact the devices ability to report events or sensor data. The device can be manually woken with a button press on the device as described below - note that triggering a device to send an event is not the same as a wakeup notification, and this will not allow the controller to communicate with the device.


Press on any button of the Soft Remote.

## Channels

The following table summarises the channels available for the Soft Remote  -:

| Channel Name | Channel ID | Channel Type | Category | Item Type |
|--------------|------------|--------------|----------|-----------|
| Scene Number | scene_number | scene_number |  | Number | 
| Battery Level | battery-level | system.battery_level | Battery | Number |

### Scene Number
Triggers when a scene button is pressed.

The ```scene_number``` channel is of type ```scene_number``` and supports the ```Number``` item.
This channel provides the scene, and the event as a decimal value in the form ```<scene>.<event>```. The scene number is set by the device, and the event is as follows -:

| Event ID | Event Description  |
|----------|--------------------|
| 0        | Single key press   |
| 1        | Key released       |
| 2        | Key held down      |
| 3        | Double keypress    |
| 4        | Tripple keypress   |
| 5        | 4 x keypress       |
| 6        | 5 x keypress       |

### Battery Level
Represents the battery level as a percentage (0-100%). Bindings for things supporting battery level in a different format (e.g. 4 levels) should convert to a percentage to provide a consistent battery level reading.

The ```system.battery-level``` channel is of type ```system.battery-level``` and supports the ```Number``` item and is in the ```Battery``` category.
This channel provides the battery level as a percentage and also reflects the low battery warning state. If the battery state is in low battery warning state, this will read 0%.


## Device Configuration

The following table provides a summary of the 8 configuration parameters available in the Soft Remote .
Detailed information on each parameter can be found in the sections below.

| Param | Name  | Description |
|-------|-------|-------------|
| 1 | Buttons 1 and 3 profile | To set-up the profile of buttons 1 and 3 |
| 2 | Buttons 2 and 4 profile | To set-up the profile of buttons 2 and 4 |
| 3 | Scene Type | To choose the way of sending Scene to the gateway |
| 4 | Button 1 configuration | To set-up the how button 1 behaves, when set in MONO Profile |
| 5 | Button 2 configuration | To set-up the how button 2 behaves, when set in MONO Profile |
| 6 | Button 3 configuration | To set-up the how button 3 behaves, when set in MONO Profile |
| 7 | Button 4 configuration | To set-up the how button 4 behaves, when set in MONO Profile |
| 8 | LED Management | How to set up LED behaviour |
|  | Wakeup Interval | Sets the interval at which the device will accept commands from the controller |
|  | Wakeup Node | Sets the node ID of the device to receive the wakeup notifications |

### Parameter 1: Buttons 1 and 3 profile

To set-up the profile of buttons 1 and 3

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Scene |
| 1 | Mono |
| 2 | Duo |

The manufacturer defined default value is ```0``` (Scene).

This parameter has the configuration ID ```config_1_1``` and is of type ```INTEGER```.


### Parameter 2: Buttons 2 and 4 profile

To set-up the profile of buttons 2 and 4

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Scene |
| 1 | Mono |
| 2 | Duo |

The manufacturer defined default value is ```0``` (Scene).

This parameter has the configuration ID ```config_2_1``` and is of type ```INTEGER```.


### Parameter 3: Scene Type

To choose the way of sending Scene to the gateway

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Central Scene |
| 1 | Scene Activation |

The manufacturer defined default value is ```0``` (Central Scene).

This parameter has the configuration ID ```config_3_1``` and is of type ```INTEGER```.


### Parameter 4: Button 1 configuration

To set-up the how button 1 behaves, when set in MONO Profile

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Control group 2 |
| 1 | All switches ON |
| 2 | All switches OFF |

The manufacturer defined default value is ```0``` (Control group 2).

This parameter has the configuration ID ```config_4_1``` and is of type ```INTEGER```.


### Parameter 5: Button 2 configuration

To set-up the how button 2 behaves, when set in MONO Profile

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Control group 3 |
| 1 | All switches ON |
| 2 | All switches OFF |

The manufacturer defined default value is ```0``` (Control group 3).

This parameter has the configuration ID ```config_5_1``` and is of type ```INTEGER```.


### Parameter 6: Button 3 configuration

To set-up the how button 3 behaves, when set in MONO Profile

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Control group 4 |
| 1 | All switches ON |
| 2 | All switches OFF |

The manufacturer defined default value is ```0``` (Control group 4).

This parameter has the configuration ID ```config_6_1``` and is of type ```INTEGER```.


### Parameter 7: Button 4 configuration

To set-up the how button 4 behaves, when set in MONO Profile

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Control group 5 |
| 1 | All switches ON |
| 2 | All switches OFF |

The manufacturer defined default value is ```0``` (Control group 5).

This parameter has the configuration ID ```config_7_1``` and is of type ```INTEGER```.


### Parameter 8: LED Management

How to set up LED behaviour

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | No LED |
| 1 | Flash Blue after button press |
| 2 | Blink to confirm command |
| 3 | Flash Blue and blink to confirm command |

The manufacturer defined default value is ```0``` (No LED).

This parameter has the configuration ID ```config_8_1``` and is of type ```INTEGER```.

### Wakeup Interval

The wakeup interval sets the period at which the device will listen for messages from the controller. This is required for battery devices that sleep most of the time in order to conserve battery life. The device will wake up at this interval and send a message to the controller to tell it that it can accept messages - after a few seconds, it will go back to sleep if there is no further communications. 

This setting is defined in *seconds*. It is advisable not to set this interval too short or it could impact battery life. A period of 1 hour (3600 seconds) is suitable in most instances.

Note that this setting does not affect the devices ability to send sensor data, or notification events.

This parameter has the configuration ID ```wakeup_interval``` and is of type ```INTEGER```.

### Wakeup Node

When sleeping devices wake up, they send a notification to a listening device. Normally, this device is the network controller, and normally the controller will set this automatically to its own address.
In the event that the network contains multiple controllers, it may be necessary to configure this to a node that is not the main controller. This is an advanced setting and should not be changed without a full understanding of the impact.

This parameter has the configuration ID ```wakeup_node``` and is of type ```INTEGER```.


## Association Groups

Association groups allow the device to send unsolicited reports to the controller, or other devices in the network. Using association groups can allow you to eliminate polling, providing instant feedback of a device state change without unnecessary network traffic.

The Soft Remote  supports 7 association groups.

### Group 1: Lifeline

The Lifeline association group reports device status to a hub and is not designed to control other devices directly. When using the Lineline group with a hub, in most cases, only the lifeline group will need to be configured and normally the hub will perform this automatically during the device initialisation.

Association group 1 supports 1 node.

### Group 2: Button 1 - Mono - Controlled nodes


Association group 2 supports 8 nodes.

### Group 3: Button 2 - Mono - Controlled nodes


Association group 3 supports 8 nodes.

### Group 4: Button 3 - Mono - Controlled nodes


Association group 4 supports 8 nodes.

### Group 5: Button 4 - Mono - Controlled nodes


Association group 5 supports 8 nodes.

### Group 6: Button 1 and 3 - Duo - Controlled nodes


Association group 6 supports 8 nodes.

### Group 7: Button 2 and 4 - Duo - Controlled nodes


Association group 7 supports 8 nodes.

## Technical Information

### Endpoints

#### Endpoint 0

| Command Class | Comment |
|---------------|---------|
| COMMAND_CLASS_NO_OPERATION_V1| |
| COMMAND_CLASS_BASIC_V1| |
| COMMAND_CLASS_ASSOCIATION_GRP_INFO_V1| |
| COMMAND_CLASS_DEVICE_RESET_LOCALLY_V1| |
| COMMAND_CLASS_CENTRAL_SCENE_V1| Linked to BASIC|
| COMMAND_CLASS_ZWAVEPLUS_INFO_V1| |
| COMMAND_CLASS_CONFIGURATION_V1| |
| COMMAND_CLASS_MANUFACTURER_SPECIFIC_V1| |
| COMMAND_CLASS_POWERLEVEL_V1| |
| COMMAND_CLASS_BATTERY_V1| |
| COMMAND_CLASS_WAKE_UP_V2| |
| COMMAND_CLASS_ASSOCIATION_V1| |
| COMMAND_CLASS_VERSION_V1| |

### Documentation Links

* [Manual](https://www.cd-jackson.com/zwave_device_uploads/250/nodon-crc-3-6-xx-userguide-150707-en-interactive.pdf)

---

Did you spot an error in the above definition or want to improve the content?
You can [contribute to the database here](http://www.cd-jackson.com/index.php/zwave/zwave-device-database/zwave-device-list/devicesummary/250).
