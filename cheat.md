#Find line matching patern and append TOAPPEND value
sed -i '/PATTERN/ s/$/TOAPPEND /'  zabbix_agentd.conf

#Get ip from eth
ifconfig |grep eth1 -A 1 | grep inet | cut -d":" -f 2 | cut -d" " -f1
