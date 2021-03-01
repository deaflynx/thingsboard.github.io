---
layout: docwithnav
title: Installing ThingsBoard Edge on Ubuntu Server
description: Installing ThingsBoard Edge on Ubuntu Server

---

* TOC
{:toc}

This guide describes how to install ThingsBoard Edge on Ubuntu Server 18.04 LTS.

{% include templates/edge/hardware-requirements.md %}

### Step 1. Install Java 8 (OpenJDK) 

{% include templates/install/ubuntu-java-install.md %}

### Step 2. Configure PostgreSQL

{% include templates/edge/ubuntu-db-postgresql.md %}

### Step 3. ThingsBoard Edge service installation

Download installation package.

```bash
wget https://dist.thingsboard.io/tb-edge-1.0.0beta.deb
```
{: .copy-code}

Go to the download repository and install ThingsBoard Edge service

```bash
sudo dpkg -i tb-edge-1.0.0beta.deb
```
{: .copy-code}

### Step 4. Configure ThingsBoard Edge

{% include templates/edge/ubuntu-configure-edge.md %}

### Step 5. Run installation script

{% include templates/edge/run-edge-install.md %} 

### Step 6. Restart ThingsBoard Edge service

```bash
sudo service tb-edge restart
```
{: .copy-code}

### Step 7. Open ThingsBoard Edge UI

{% include templates/edge/open-edge-ui.md %} 

### Troubleshootings

ThingsBoard Edge logs stored in the following directory:
 
```bash
/var/log/tb-edge
```

You can issue the following command in order to check if there are any errors on the service side:
 
```bash
cat /var/log/tb-edge/tb-edge.log | grep ERROR
```

{% include templates/edge/edge-service-commands.md %} 

## Next Steps

{% include templates/edge/install/next-steps.md %}