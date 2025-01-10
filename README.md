# PMF-Developer-Kit
MobileFoundation Developer Kit Zip for Mac, Linux and Windows
Persistent Mobile Foundation : PMF-9.1.0-20241220161835.zip


Abstract :
This is the development kit package for PMF 9.1.


Date: December 20, 2024

Contents:

1.0 Prerequisites for the running PMF 9.1 development kit
2.0 Steps to set up development kit
3.0 How to access the consoles
4.0 How to check server logs


1.0 Prerequisites
===============================================
The following software must be installed before running the development kit:
1. Java 17
2. Java 8


2.0 Steps to set up development kit:
===============================================
1. Unzip the development kit zip file.
2. Navigate to <PMF_development_kit_DIR>\mfp-server\usr\servers\mfp and edit server.env
	2a. Set JAVA_HOME path to JAVA 17
3. Navigate to <PMF_development_kit_DIR>\mfp-server\usr\servers\analytics and edit server.env
	3a. Set JAVA_HOME path to JAVA 8
4. [OPTIONAL] To access the console from remote machine instead of localhost update the following.
	4a. Edit <PMF_development_kit_DIR>\mfp-server\usr\servers\mfp\bootstrap.properties and set mfp.server.host variable to PMF server IP
	4b. Edit <PMF_development_kit_DIR>\mfp-server\usr\servers\analytics\bootstrap.properties and set mfp.server.host variable to PMF server IP
	4c. Edit <PMF_development_kit_DIR>\mfp-server\usr\servers\analytics\server.env and add CONFIGURATION_FILE_PATH=<PMF_development_kit_DIR>\mfp-server\usr\servers\analytics\config.properties
	4d. Navigate to <PMF_development_kit_DIR>\mfp-server\usr\servers\analytics and edit config.properties
		and set allowed.hostname to hostname or IP of the PMF server machine.
5. Use below scripts to start/stop server from <PMF_development_kit_DIR>
	5a. For Windows:
		run.cmd - Start the servers
		stop.cmd - Stop the servers
	5b. For Linux:
		run.sh - Start the servers
		stop.sh - Stop the servers

		
3.0 How to access the consoles 
======================================================
Navigate to the below links on browser:

PMF Admin Console => http://localhost:9080/mfpconsole/
PMF Application Center Console => http://localhost:9080/appcenterconsole/
PMF Analytics Console => http://localhost:9081/analytics/


4.0 How to check server logs
===============================================
Navigate to the following location to check the server logs:

1. mfp server - <PMF_development_kit_DIR>\mfp-server\usr\servers\mfp\logs
2. analytics server - <PMF_development_kit_DIR>\mfp-server\usr\servers\analytics\logs
