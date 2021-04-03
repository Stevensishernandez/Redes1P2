# Redes1P2
VLANs, VTP, STP


## Distribucion de ip's  📄
| Dispositivo | VLAN  | Dirección IP  | Mascada de red| Gateway | Virtualizada Si/No |
| ------------- | ------------- | -------------| ------------- | ------------- | ------------- |
| ADMIN 1 f1/9 | 10 | 192.168.116.10 | 255.255.255.192 | 192.168.116.1 | NO | 
| ADMIN 2 f1/9 | 10 | 192.168.116.11 | 255.255.255.192 | 192.168.116.1 | NO |
| PC1 (CONTA1) | 20 | 192.168.116.70 | 255.255.255.192 | 192.168.116.65 | SI | 
| PC2 (CONTA2) | 20 | 192.168.116.71 | 255.255.255.192 | 192.168.116.65 | NO |
| WEBCONTA f1/12 | 20 | 192.168.116.72 | 255.255.255.192 | 192.168.116.65 | SI |
| PC3 (VENTAS1) | 30 | 192.168.116.135 | 255.255.255.192 | 192.168.116.129 | SI |
| PC4 (VENTAS2) | 30 | 192.168.116.136 | 255.255.255.192 | 192.168.116.129 | NO |
| WEBPAGE f1/10 | 30 | 192.168.116.137 | 255.255.255.192 | 192.168.116.129 | SI |
| PC5 (INFORMATICA) | 30 | 192.168.116.138 | 255.255.255.192 | 192.168.116.129 | NO |
| BD f1/11 | 30 | 192.168.116.139 | 255.255.255.192 | 192.168.116.129 | SI |

# Topologia1 .


### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW8 y ESW9 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW9 y ESW10 | 2 enlaces | f1/3 - 4 |
| Po3 | Entre ESW8 y ESW10 | 2 enlaces | f1/5 - 6 |

# Topologia3


### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW5 y ESW6 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW6 y ESW7 | 2 enlaces | f1/3 - 4 |
| Po3 | Entre ESW5 y ESW7 | 2 enlaces | f1/5 - 6 |
| Po4 | Entre ESW6 y ESW11 | 2 enlaces | f1/7 - 8 |
| truncal | SWC3 y SWC2 |  | f1/1  |




