Edit ThingsBoard Edge configuration file 
```bash 
sudo nano /etc/tb-edge/conf/tb-edge.conf
``` 
{: .copy-code}

**Uncomment and put your** cloud connection settings:
* Replace "PUT_YOUR_EDGE_KEY_HERE" and "PUT_YOUR_EDGE_SECRET_HERE" with edge **key and secret** respectively.

{% capture local-deployment %}

* ThingsBoard **Edge** by default is configured to be connected to the ThingsBoard **Live Demo**. Uncomment and replace CLOUD_RPC_HOST with an IP address of the machine where ThingsBoard **Professional Edition/Community Edition** server is running. Or replace it with **localhost** in case ThingsBoard Edge is running on the same machine where cloud instance is running.

* If ThingsBoard Edge is going to be running on the same machine where ThingsBoard **Professional Edition/Community Edition** server is running please uncomment HTTP/MQTT/COAP bind ports to avoid port collisions. Please make sure those ports are not used by any other application.

* If you have changed default PostgreSQL database name (**tb_edge**), username (**postgres**) or password (**postgres**) in [Step 2](/docs/edge/install/deb-installation/#step-2-configure-postgresql), please also uncomment and edit corresponding lines.

{% endcapture %}

{% include templates/info-banner.md content=local-deployment %}

