# kibana-installation-on-ubuntu20.04

This is a guide for Kibana installation on Ubuntu 20.04

## Step 1 - Prepare the Environment

Install java11 - You can follow this guideline to install java ([https://github.com/ozgunakin/java-installation-on-ubuntu20.04](https://github.com/ozgunakin/java-installation-on-ubuntu20.04))

Install Elasticsearch - You can follow this guideline to install Elasticsearch ([https://github.com/ozgunakin/elasticsearch-installation-on-ubuntu20.04](https://github.com/ozgunakin/elasticsearch-installation-on-ubuntu20.04))

## Step 2 - Install Kibana with Apt

Install latest version ap kibana using apt package manager.

```
sudo apt update 
sudo apt install kibana
```

## Step 3 - Configure Elasticsearch

Edit Kibana yml file which is placed in /etc/kibana.

```
sudo nano /etc/kibana/kibana.yml
```

Change the following line and save the file.

> server.port: 5601  #unhash it if it is hashed
>
> server.host =0.0.0.0      #sholud be chaged to be able to elastic from remote server

## Step 4 - Start & Enable Kibana

Start Kibana service.

```
sudo service kibana start
```

Enable Kibana service.

```
sudo systemctl enable kibana
```

## Step 5 - Connect Kibana UI

You can connect Kibana over "your-ip-address:5601" from your browser.

![](.gitbook/assets/image.png)
