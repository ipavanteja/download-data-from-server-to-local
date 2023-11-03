**Download Files and Folders from an Ubuntu Server** 

**Step-1: Login and Update** 

Login into your server with ssh and update your Ubuntu server with sudo apt update 

sudo apt upgrade 

**Step-2: Install necessary tools** 

Install net-tools:**  

sudo apt install net-tools** Install python3: 

sudo apt install python3 Install zip 

sudo apt install zip 

**Step-3: Start a python3 http server** 

Start a python server on server’s root folder using python3 Python3 –m http.server <port\_number> 

**Step-4: Access the server and download files** 

Open any browser in your local machine(system) and access your server IP with port number **Note:** You can find your server’s IP with ifconfig command 

Now you can be able to see all the files and folders which are there in your server. 

You can simply download any file by pressing right click and ‘save file as’ 

**Note:** You cannot download the whole folder.  

If you want to download the whole folder, you need to zip the folder first 

**Step-5: zip the folders** 

Zip all the folders that you want to download using zip command For example, to compress a folder named "myfolder," you can use: zip -r myfolder.zip myfolder 

**Step-6: Start the python server and download the zip files** 

Start the python server using python3 

You can simply download the zip files by clicking on them. 

Once you download all the files and folders stop the python server with ctrl+c keyboard shortcut and exit from ssh connection with exit command 
