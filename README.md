# SmartDustbin
#The main aim of this project is to develop an intelligent dustbin which can monitor waste through sensors and gives the information in detailed which are connected to internet. Initially all the sensors from different location are connected through Internet in every location sensors will measure and calculate the waste and information will be sent to the server. At Server it will Process the information and sent it to the concern Authorities to take necessary action.
#Connect the sensors and the raspberry pi as per the connections given above.
#Open the terminal of raspberry pi and import the libraries first.
#Use the following commands for the library installation of ultrasonic sensor.
 	  
 	  		
 	  		sudo apt-get update
 	  		sudo apt-get install rpi.gpio
 	 
#Use the following commands for the library installation of accelerometer sensor.

 	  sudo apt-get install build-essential bibi2c-dev i2c-tools   
 	  python-dev libffi-dev
 	  pip install smbus-cffi
 	  pip install git+https://github.com/bivab/smbus-cffi.git
 	  
 #Then clone the repository from github.
 	  
    git clone https://github.com/bivab/smbus-cffi.git
 	  python setup.py install
 #Use the following commands for the library installation for email alert.
 	 
    sudo apt-get install ssmtp
 	  sudo apt-get install mailutils
 #Now edit the SSMTP configuration file
 	
 	  sudo nano /etc/ssmrp/ssmtp.conf
 
 #It needs to include this:
 	
 	  	root=postmaster
 	  	mailhub=smtp.gmail.com:587
 	  	hostname=raspberrypi
 	  	AuthUser=sendername@gmail.com
 	  	AuthPass=Password
 	  	UseSTARTTLS=YES
