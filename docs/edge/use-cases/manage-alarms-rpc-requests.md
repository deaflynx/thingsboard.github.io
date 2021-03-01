---
layout: docwithnav
title: Manage alarms and RPC requests on edge devices
description: ThingsBoard Edge use case #1

configureAlarmRulesCE:
    0:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-1.png
        title: 'Login to your ThingsBoard <b>CE</b> instance and open Device profiles page.'
    1:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-2.png
        title: 'Click "+" to add new device profile.'
    2:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-3.png
        title: 'Input device profile name. For example, type "edge thermostat". Click "Transport configuration" to proceed.'
    3:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-4.png
        title: 'For this example we will use default transport configuration. Click "Alarm rules" to proceed.'        
    4:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-5.png
        title: 'Click "Add alarm rule" button.'
    5:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-6.png
        title: 'Specify alarm type. For example, "High temperature". Click "+" icon to add new alarm condition.'
    6:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-7.png
        title: 'Click "Add key filter" button.'
    7:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-8.png
        title: 'Select key type, input key name, select value type and click "Add".'
    8:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-9.png
        title: 'Select operation and input threshold value. Click "Add".'
    9:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-10.png
        title: 'Click "Save" button.'
    10:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-11.png
        title: 'Click "Add" button.'
    11:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-12.png
        title: 'Newly create device profile will be show first in the list, because default sort order is by created time.'

configureAlarmRulesEdge:
    0:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-13.png
        title: 'Login to your ThingsBoard <b>Edge</b> instance and open Device profiles page.'
    1:
        image: /images/edge/use-cases/manage-alarms/configure-rules-item-14.png
        title: 'Verify that "edge thermostat" was provisioned to edge as well.'

provisionDevicesEdge:
    0:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-1.png
        title: 'Login to your ThingsBoard <b>Edge</b> instance and open Device groups page.'
    1:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-2.png
        title: 'Open "All" device group.'
    2:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-3.png
        title: 'Click on the "Add Device"("+") icon in the top right corner of the table.'
    3:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-4.png
        title: 'Input device name. For example, "DHT22". Select "edge thermostat" from device profiles list. No other changes required at this time. Click "Add" to add the device.'
    4:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-5.png
        title: 'Now your "DHT22" device should be listed first, since table sort devices using created time by default. Click "Add" to add one more device.'
    5:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-6.png
        title: 'Input device name. For example, "Air Conditioner". No other changes required at this time. Click "Add" to add the device.'
    6:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-7.png
        title: 'Now your "Air Conditioner" device should be listed first, since table sort devices using created time by default.'
    7:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-8.png
        title: 'Click on "DHT22" device row to open device details and navigate to "Relations" tab. Click "+" icon to add new relation.'
    8:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-9.png
        title: 'Specify relation type "Manages" and select "Air Conditioner" device from the list. Click "Add" to add this relation. Now we verify that devices were provisioned to cloud.'

provisionDevicesCE:    
    0:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-10.png
        title: 'Login to your ThingsBoard <b>CE</b> instance and open Devices page.'
    1:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-11.png
        title: 'Make sure that "DHT22" and "Air Conditioner" devices are in the devices list.'
    2:
        image: /images/edge/use-cases/manage-alarms/provision-devices-item-12.png
        title: 'Verify that relation from "DHT22" to "Air Conditioner" was provisioned as well.'

rootRuleChainPreview:
    0:
        image: /images/edge/use-cases/manage-alarms/root-rule-chain.png

updateRootRuleChainCE:
    0:
        image: /images/edge/use-cases/manage-alarms/update-root-item-1.png
        title: 'Login to your ThingsBoard <b>CE</b> instance and open Rule chain templates page.'
    1:
        image: /images/edge/use-cases/manage-alarms/update-root-item-2.png
        title: 'Open default "Edge Root Rule Chain".'
    2:
        image: /images/edge/use-cases/manage-alarms/update-root-item-3.png
        title: 'Filter node by "script" word and drag script node (Transformation) to rule chain.'
    3:
        image: /images/edge/use-cases/manage-alarms/update-root-item-4.png
        title: 'Input node name and add <b>JavaScript</b> code (you can copy and paste it from the snippet above) to create proper <b>enable</b> command for Air Conditioner device. Click "Add" to proceed.'
    4:
        image: /images/edge/use-cases/manage-alarms/update-root-item-5.png
        title: 'Drag connection from "Device Profile Node" to newly added <b>enabled</b> script node.'
    5:
        image: /images/edge/use-cases/manage-alarms/update-root-item-6.png
        title: 'Select "Alarm Created" from the list and click "Add" button.'
    6:
        image: /images/edge/use-cases/manage-alarms/update-root-item-7.png
        title: 'Click "Apply changes" to save current progress.'
    7:
        image: /images/edge/use-cases/manage-alarms/update-root-item-8.png
        title: 'Filter rule nodes by "change" word and add "change originator" node to rule chain.'
    8:
        image: /images/edge/use-cases/manage-alarms/update-root-item-9.png
        title: 'Select "Related" source. Select "Manages" filter. Select "Device" type. Click "Add".'
    9:
        image: /images/edge/use-cases/manage-alarms/update-root-item-10.png
        title: 'Add "Success" relations from script node to change originator. Add "Success" relation from change originator to RPC Call Request node. Save changes.'

updateRootRuleChainEdge:
    0:
        image: /images/edge/use-cases/manage-alarms/update-root-item-11.png
        title: 'Login to your ThingsBoard <b>Edge</b> instance and open Rule chains page.'
    1:
        image: /images/edge/use-cases/manage-alarms/update-root-item-12.png
        title: 'Open "Edge Root Rule Chain".'
    2:
        image: /images/edge/use-cases/manage-alarms/update-root-item-13.png
        title: 'Verify that rule chain is the same as you have updated on cloud.'

copyAccessTokenAirConditioner:
    0:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-1.png
        title: 'Open Device groups page in the ThingsBoard <b>Edge</b> instance.'
    1:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-2.png
        title: 'Open "All" device group.'
    2:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-3.png
        title: 'Click on the <b>Air Conditioner</b> device row in the table to open device details.'
    3:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-4.png  
        title: 'Click "Copy access token". Token will be copied to your clipboard. Save it to a safe place.'

copyAccessTokenDht22:
    0:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-1.png
        title: 'Open Device groups page in the ThingsBoard <b>Edge</b> instance.'
    1:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-2.png
        title: 'Open "All" device group.'
    2:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-5.png
        title: 'Click on the <b>DHT22</b> device row in the table to open device details.'
    3:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-6.png  
        title: 'Click "Copy access token". Token will be copied to your clipboard. Save it to a safe place.'

deviceAlarmTab:
    0:
        image: /images/edge/use-cases/manage-alarms/copy-access-token-item-3.png
        title: 'Click on the <b>DHT22</b> device row in the table to open device details.'
    1:
        image: /images/edge/use-cases/manage-alarms/device-alarm-tab-item-1.png
        title: 'Navigate to the alarm tab.'

mqttWindows:
    0:
        image: /images/edge/getting-started/mqtt-windows-item-1.png
        title: 'Create new MQTT Client with the properties listed in screenshots below.'
    1:
        image: /images/edge/getting-started/mqtt-windows-item-2.png
        title: 'Populate the topic name and payload. Make sure the payload is a valid JSON document. Click "Publish" button.'

---
* TOC
{:toc}

## Use case
Let's assume you have a warehouse with two devices connected to ThingsBoard **Edge**: 
* DHT22 temperature sensor
* Air Conditioner 

ThingsBoard Edge has the following responsibilities:
 * **Collects temperature readings** from the DHT22 sensor
 * **Creates and updates alarms** if the temperature in the warehouse is higher than 50 °C
 * In case if the temperature becomes critical, ThingsBoard Edge turns on the cooler system by **sending RPC call requests** to the Air Conditioner device
 * **Pushes telemetry to the cloud**

Please note that this is just a simple theoretical use case to demonstrate the capabilities of the platform. 
You can use this tutorial as a basis for much more complex scenarios.

## Prerequisites

{% include templates/edge/use-cases/ce-prerequisites.md %}

## Configure Alarm Rules

We will use [alarm rules](/docs/user-guide/device-profiles/#alarm-rules) feature to raise alarm when temperature reading is greater than 50 °C degrees.
For this purpose, we should create new device profile and add new alarm rule. We recommend creating dedicated [device profiles](/docs/user-guide/device-profiles/) for each corresponding device type. Let's create new device profile "edge thermostat".

{% include images-gallery.html imageCollection="configureAlarmRulesCE" showListImageTitles="true" %}

Please open ThingsBoard **Edge** UI using the URL: [http://localhost:18080](http://localhost:18080) to see provisioned device profiles.

{% include templates/edge/bind-port-changed-banner.md %}

{% include images-gallery.html imageCollection="configureAlarmRulesEdge" showListImageTitles="true" %}

## Provision devices

For simplicity, we will provision device manually using the UI.

Let's first create **DHT22 temperature sensor** and **Air Conditioner** devices on the edge and add relation between these devices. This relation will be used to find related **Air Conditioner** device once **DHT22 temperature sensor** will send critical temperature value.

We are going to provision device on the Edge. Please open ThingsBoard **Edge** UI using the URL: [http://localhost:18080](http://localhost:18080).

{% include templates/edge/bind-port-changed-banner.md %}

{% include images-gallery.html imageCollection="provisionDevicesEdge" showListImageTitles="true" %}

Please open ThingsBoard **CE** using the URL [http://localhost:8080](http://localhost:8080) or [Live Demo](https://demo.thingsboard.io):

{% include images-gallery.html imageCollection="provisionDevicesCE" showListImageTitles="true" %}

## Configure edge rule engine to handle alarms and send RPC calls

We are going to update "Edge Root Rule Chain" that will handle **Alarm Created** events for "DHT22" sensor and will send appropriate commands to the "Air Conditioner" device.
Here is the final configuration of edge root rule chain:

{% include images-gallery.html imageCollection="rootRuleChainPreview" %}

In the next steps we are going to create **JavaScript** node to create appropriate RPC commands to the **Air Conditioner** device.
JavaScript for script node that will emulate enabling of Air Conditioner:

{% highlight javascript %}
var newMsg = {};
newMsg.method = "enabled_air_conditioner";
newMsg.params = {"speed": 1.0};
return {msg: newMsg, metadata: metadata, msgType: msgType}; {% endhighlight %}

Please use this snippet in the next steps, if required.

Here are the steps to update default edge "Root Rule Chain" to the rule chain above:

{% include images-gallery.html imageCollection="updateRootRuleChainCE" showListImageTitles="true" %}

Now let's open ThingsBoard **Edge** UI to see updated root rule chain:

{% include images-gallery.html imageCollection="updateRootRuleChainEdge" showListImageTitles="true" %}

## Connect "Air Conditioner" to edge and subscribe for RPC commands

To subscribe to RPC commands from edge for the **Air Conditioner** device you need to get the **Air Conditioner** device credentials first.
ThingsBoard supports different device credentials. We recommend to use default auto-generated credentials which is access token for this guide.

Please open ThingsBoard **Edge** UI using the URL: [http://localhost:18080](http://localhost:18080).

{% include templates/edge/bind-port-changed-banner.md %}

{% include images-gallery.html imageCollection="copyAccessTokenAirConditioner" showListImageTitles="true" %}

Now you are ready to subscribe to RPC commands for Air Conditioner device.
We will use simple commands to subscribe to RPC commands over MQTT protocol in this example.

Please download following scripts to your local folder:
- [**mqtt-js.sh**](/docs/edge/use-cases/resources/manage-alarms-rpc-requests/mqtt-js.sh)
- [**cooler.js**](/docs/edge/use-cases/resources/manage-alarms-rpc-requests/cooler.js)

**NOTE** We assume that you have Node.js and NPM installed on your local PC.

Before running the scripts, please modify **mqtt-js.sh** accordingly:

- Replace **YOUR_ACCESS_TOKEN** with **Air Conditioner** device access token copied from the steps above. 

- Replace **YOUR_TB_EDGE_HOST** with your ThingsBoard Edge host. For example, **localhost**.

- Replace **YOUR_TB_EDGE_MQTT_PORT** with your ThingsBoard Edge MQTT port. For example, **11883** or **1883**.

Open the terminal, go to the folder that contains **mqtt-js.sh** and **cooler.js** scripts and make sure it is executable:
```shell
 chmod +x *.sh
```

Install **mqtt** node module to be able to use mqtt package in the **cooler.js** script:
```shell
node install mqtt
```

Then run the following command:
```shell
bash mqtt-js.sh
```

You should see the following screen with your host and device token:

```shell
pc@pc-XPS-15-9550:~/alarm-tutorial$ bash mqtt-js.sh
Connecting to: localhost:11883 using access token: sFqoF18PTyViO8L0qo7c
Cooler is connected!
```

**NOTE** Please open a new terminal tab to push temperature telemetry to device and leave this running in the background until end of the guide.

## Post telemetry to "DHT22" sensor to create alarm

To post temperature telemetry to the **DHT22** sensor you need to get the **DHT22** sensor credentials first.
ThingsBoard support different device credentials. We recommend to use default auto-generated credentials which is access token for this guide.

Please open ThingsBoard **Edge** UI using the URL: [http://localhost:18080](http://localhost:18080).

{% include templates/edge/bind-port-changed-banner.md %}

{% include images-gallery.html imageCollection="copyAccessTokenDht22" showListImageTitles="true" %}

Now you are ready to publish temperature telemetry data on behalf of your device.
We will use simple commands to publish temperature data over HTTP or MQTT in this example.

{% capture connectdevicetogglespec %}
HTTP<small>Linux, macOS or Windows</small>%,%http%,%templates/edge/getting-started/http.md%br%
MQTT<small>Linux or macOS</small>%,%mqtt-linux%,%templates/edge/getting-started/mqtt-linux.md%br%
MQTT<small>Windows</small>%,%mqtt-windows%,%templates/edge/getting-started/mqtt-windows.md%br%
CoAP<small>Linux or macOS</small>%,%coap%,%templates/edge/getting-started/coap.md{% endcapture %}
{% include content-toggle.html content-toggle-id="connectdevice" toggle-spec=connectdevicetogglespec %}

Once you have successfully published the "temperature" readings with value **51**:

{% capture connectdevicetogglespec %}
HTTP<small>Linux, macOS or Windows</small>%,%http%,%templates/edge/use-cases/manage-alarms/http-above-threshold.md%br%
MQTT<small>Linux or macOS</small>%,%mqtt-linux%,%templates/edge/use-cases/manage-alarms/mqtt-linux-above-threshold.md%br%
MQTT<small>Windows</small>%,%mqtt-windows%,%templates/edge/use-cases/manage-alarms/mqtt-windows-above-threshold.md%br%
CoAP<small>Linux or macOS</small>%,%coap%,%templates/edge/use-cases/manage-alarms/coap-above-threshold.md{% endcapture %}
{% include content-toggle.html content-toggle-id="connectdevice" toggle-spec=connectdevicetogglespec %}

You should immediately see alarm in the Device Alarm Tab:

{% include images-gallery.html imageCollection="deviceAlarmTab" showListImageTitles="true" %}

## Verify that RPC request was send to "Air Conditioner" device

Open the terminal where **mqtt-js.sh** script is running. 
You should see similar messages on the screen:

```shell
pc@pc-XPS-15-9550:~/alarm-tutorial$ bash mqtt-js.sh
Connecting to: localhost:11883 using access token: sFqoF18PTyViO8L0qo7c
Cooler is connected!
Received RPC command from edge!
Method: enabled_air_conditioner
Speed params: 1
```

Congratulations! RPC request was successfully sent to **Air Conditioner** device based on the temperature readings from the **DHT22** sensor.

## Next Steps

{% assign currentGuide = "ManageAlarmsAndRpcRequestsOnEdgeDevices" %}{% include templates/edge/guides-banner-edge.md %}