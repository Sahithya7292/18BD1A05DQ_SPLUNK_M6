# 18BD1A05DQ_SPLUNK_M6
SIEM(Security Information And Event Management)-Splunk


Splunk is a software used to analyze large amount of data.This captures, indexes and correlates real-time data in a searchable repository from which it can generate graphs, reports, alerts, dashboards and visualizations.

# 1.Using Docker
From Command Prompt

# -> docker images
(To check if any image is present or not)
![image](https://user-images.githubusercontent.com/72086151/124495655-01ed4980-ddd6-11eb-95aa-84b1e9222a82.png)

# -> docker pull splunk/splunk:latest
(pull the splunk/splunk image's latest version)

# -> docker network create --driver bridge --attachable kmit
(create a network - a hexadecimal code is generated)

# -> docker run --network kmit --name splunkE --hostname splunkE -p 8001:8000 -e "SPLUNK_PASSWORD=administrator" -e "SPLUNK_START_ARGS=--accept-license" -it splunk/splunk:latest

# -> docker ps
(to check if any network is running)

# -> docker pull splunk/universalforwarder:latest

# -> docker run --network kmit --name SUF --hostname SUF -e "SPLUNK_PASSWORD=administrator" -e "SPLUNK_START_ARGS=--accept-license" -e "SPLUNK_STANDALONE_URL=splunkE" -it splunk/universalforwarder:latest

# Open http://localhost:8001/ enter the password and any username as written in run command of the network and click sign in

# 2.Using https://tryhackme.com/room/bpsplunk
