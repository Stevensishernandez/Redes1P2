# Redes1P2
VLANs, VTP, STP


## Distribucion de ip's  📄
| Dispositivo | VLAN  | Dirección IP  | Mascada de red| Gateway |
| ------------- | ------------- | -------------| ------------- | ------------- |
| ADMIN 1 f1/9 | 10 | 192.168.116.10 | 255.255.255.192 | 192.168.116.1 |
| ADMIN 2 f1/9 | 10 | 192.168.116.11 | 255.255.255.192 | 192.168.116.1 |
| PC1 (CONTA1) | 20 | 192.168.116.70 | 255.255.255.192 | 192.168.116.65 |
| PC2 (CONTA2) | 20 | 192.168.116.71 | 255.255.255.192 | 192.168.116.65 |
| WEBCONTA f1/12 | 20 | 192.168.116.72 | 255.255.255.192 | 192.168.116.65 |
| PC3 (VENTAS1) | 30 | 192.168.116.135 | 255.255.255.192 | 192.168.116.129 |
| PC4 (VENTAS2) | 30 | 192.168.116.136 | 255.255.255.192 | 192.168.116.129 |
| WEBPAGE f1/10 | 30 | 192.168.116.137 | 255.255.255.192 | 192.168.116.129 |
| PC5 (INFORMATICA) | 30 | 192.168.116.138 | 255.255.255.192 | 192.168.116.129 |
| BD f1/11 | 30 | 192.168.116.139 | 255.255.255.192 | 192.168.116.129 |

# Topologia1 .

### Configuraciones
| Virtualizada Si/No | HOST |Servidor|
| ------------- | ------------- | ------------- |
| No | Admin1 | -- |
| No | Admin2 | -- |
| Si | Server_Contabilidad | WEBCONTA |
| Si | Server_Ventas | WEBPAGE |
| Si | Server_Informatica  | BD |

### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW8 y ESW9 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW9 y ESW10 | 2 enlaces | f1/3 - 4 |
| Po3 | Entre ESW8 y ESW10 | 2 enlaces | f1/5 - 6 |



