![nmap](/assets/nmap.png)


## NMAP introduction ##

Un segment de réseau est un groupe d'ordinateurs connectés à l'aide d'un support partagé. Par exemple, le support peut être un commutateur Ethernet ou un point d'accès WiFi. Dans un réseau IP, un sous-réseau est généralement l'équivalent d'un ou plusieurs segments de réseau connectés ensemble et configurés pour utiliser le même routeur. Le segment de réseau fait référence à une connexion physique, tandis qu'un sous-réseau fait référence à une connexion logique.

```shell
#Scan avec nmap
utilisateur@ip$ nmap -iL list_of_hosts.txt
utilisateur@ip$ nmap -sL TARGETS
utilisateur@ip$ sudo nmap -PP -sn 10.10.68.220/24

#Scan avec Masscan
utilisateur@ip$ masscan MACHINE_IP/24 -p443
utilisateur@ip$ masscan MACHINE_IP/24 -p80,443
utilisateur@ip$ masscan MACHINE_IP/24 -p22-25
utilisateur@ip$ masscan MACHINE_IP/24 ‐‐top-ports 100
```

Option pour nmap :
**-pp** : ICMP timestamp
**-pm** : ICMP addresse mask
**-pe** : ICMP echo



