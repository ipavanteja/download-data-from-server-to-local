# **Download Files and Folders from an Ubuntu Server** 

## **Step-1: Login and Update** 

Login into your server with ssh and update your Ubuntu server with sudo apt update 
```
sudo apt upgrade
```
```
sudo apt update
```

## **Step-2: Install necessary tools** 

Install net-tools: 
```
sudo apt install net-tools
```

Install python3: 
```
sudo apt install python3 
```

Install zip: 
```
sudo apt install zip 
```

## **Step-3: Start a python http server** 

Start a python server on the server’s root folder using python3 
```
python3 –m http.server <port_number> 
```

If you want to start a python server on a specific IP, you can do like this,
```
python3 -m http.server <port_number> --bind <server-IP>
```
### Firewall Settings on the Server (if required)

Ensure that the firewall on your Ubuntu Server allows incoming traffic on the custom port you specified. 
You may need to configure your server's firewall rules to allow traffic on that port.

If you're using ufw on Ubuntu, you can add a rule to allow traffic on your custom port like this:
```
sudo ufw allow <custom-port>/tcp
```
```
sudo ufw reload
```

## **Step-4: Access the server and download files** 

Open any browser in your local machine(system) and access your server IP with the port number 

**Note:** You can find your server’s IP with `ifconfig` command 

Now you can be able to see all the files and folders which are there on your server. 

You can simply download any file by pressing right-click and ‘save file as’ 

**Note:** You cannot download the whole folder.  

If you want to download the whole folder, you need to 'zip the folder first' 

## **Step-5: zip the folders** 

Zip all the folders that you want to download using `zip` command.

For example, to compress a folder named "myfolder," you can use: 
```
zip -r myfolder.zip myfolder 
```

## **Step-6: Start the python server and download the zip files** 

Start the python server using python3 

You can simply download the zip files by clicking on them. 

Once you download all the files and folders stop the python server with the ctrl+c keyboard shortcut and exit from the ssh connection with `exit` command 
