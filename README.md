# Qradar_IP_Context_menu.xml


This is investigate right-click integration for use within IBM Security QRadar SIEM using the built-in ip_context_menu.xml file - located on the QRadar console in the /opt/qradar/conf/ directory.
       
        <menuEntry name="virustotal_IP" url="https://www.virustotal.com/en/ip-address/%IP%/information/"/>
        <menuEntry name="OpenDNS Investigate Lookup" url="https://investigate.opendns.com/ip-view/%IP%"/>
        <menuEntry name="TCPUTILS_Lookup" url="http://www.tcpiputils.com/browse/ip-address/%IP%"/>
        <menuEntry name="X-Force Exchange Lookup" url="https://exchange.xforce.ibmcloud.com/#/ip/%IP%" />
        <menuEntry name="IPVOID Check" url="http://www.ipvoid.com/scan/%IP%/"/>
        <menuEntry name="Dshield" url="http://dshield.org/ipinfo.html?ip=%IP%"/>
        <menuEntry name="MultiRBL" url="http://multirbl.valli.org/lookup/%IP%.html"/>
        <menuEntry name="SenderBase" url="http://www.senderbase.org/lookup/?search_string=%IP%"/>
        <menuEntry name="Zeus_Tracker" url="https://zeustracker.abuse.ch/monitor.php?search=%IP%"/>
        <menuEntry name="Ransomware_Tracker" url="https://ransomwaretracker.abuse.ch/tracker/?search=%IP%"/>
        <menuEntry name="Mcafee_IP" url="http://www.mcafee.com/threat-intelligence/ip/default.aspx?ip=%IP%"/>


Installation _ Guide 

Clone the repository locally or download the ip_context_menu.xml file.

Upload the ip_context_menu.xml file to your QRadar console.

$ scp ip_context_menu.xml username@<QRadar console IP>:.

Using SSH, log in to QRadar as the root user:
$ ssh username@<QRadar console IP>

Back up your existing ip_context_menu.xml file:
$ mv /opt/qradar/conf/ip_context_menu.xml /opt/qradar/conf/ip_context_menu.xml.bak

Copy your new ip_context_menu.xml file into the configuration directory:
$ cp ~/ip_context_menu.xml /opt/qradar/conf/ip_context_menu.xml

Note: Copy any previous settings from your original ip_context_menu.xml file into this new file, if required.

Restart the tomcat service:
# service tomcat restart

Contributors

Abdulrahman, Sr. Security Expert
OM
Twitter: @abdulmyid
