# Pracitca 2, Redes de computadoras 1

## Objetivos

- Configuraciones básicas del Switch y Etherswitch
- Crear y administrar VLANs 
- Crear y administrar protocolo VTP
- Crear y administrar protocolo STP 

## Direcciones privadas de las computadoras 
- Maquina1 (Steven Sis) 10.0.8.1
- Maquina2 (Miguel Solis) 10.0.8.2
- Maquina1 (Jesus Mansilla) 10.0.8.3


## Distribucion de ip's  📄
| Dispositivo | puerto | VLAN  | Dirección IP  | Mascada de red| Gateway | Virtualizada Si/No | sw |
| ------------- | ------------- | ------------- | -------------| ------------- | ------------- | ------------- | ------------- |
| ADMIN 1 | f1/9 | 10 | 192.168.116.10 | 255.255.255.192 | 192.168.116.1 | NO | ESW8 |
| ADMIN 2 | f1/9 | 10 | 192.168.116.11 | 255.255.255.192 | 192.168.116.1 | NO | ESW10 |
| PC1 (CONTA1) | p7 | 20 | 192.168.116.70 | 255.255.255.192 | 192.168.116.65 | NO | ETHR3 |
| PC2 (CONTA2) | f1/12 | 20 | 192.168.116.71 | 255.255.255.192 | 192.168.116.65 | SI | ESW11 |
| WEBCONTA | f1/12 | 20 | 192.168.116.72 | 255.255.255.192 | 192.168.116.65 | SI | ESW9 |
| PC3 (VENTAS1) | p3 | 30 | 192.168.116.135 | 255.255.255.192 | 192.168.116.129 | SI | ETHR3 |
| PC4 (VENTAS2) | p3 | 30 | 192.168.116.136 | 255.255.255.192 | 192.168.116.129 | NO | ETHR4 |
| WEBPAGE | f1/10 | 30 | 192.168.116.137 | 255.255.255.192 | 192.168.116.129 | SI | ESW9 | 
| PC5 (INFORMATICA) | p5 | 30 | 192.168.116.138 | 255.255.255.192 | 192.168.116.129 | NO | ETHR4 |
| BD | f1/11 | 30 | 192.168.116.139 | 255.255.255.192 | 192.168.116.129 | SI | ESW9 |

# Topologia1 .


### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW8 y ESW9 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW9 y ESW10 | 2 enlaces | f1/3 - 4 |
| Po3 | Entre ESW8 y ESW10 | 2 enlaces | f1/5 - 6 |

# Topologia2


### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW1 y ESW2 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW1 y ESW3 | 3 enlaces | f1/3 - 5 |
| Po3 | Entre ESW1 y ESW4 | 3 enlaces | f1/6 - 8 |
| Po4 | Entre ESW2 y ESW3 | 3 enlaces | f1/9 - 11 |
| Po5 | Entre ESW2 y ESW4 | 3 enlaces | f1/12 - 14 |

# Topologia3


### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW5 y ESW6 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW6 y ESW7 | 2 enlaces | f1/3 - 4 |
| Po3 | Entre ESW5 y ESW7 | 2 enlaces | f1/5 - 6 |
| Po4 | Entre ESW6 y ESW11 | 2 enlaces | f1/7 - 8 |
| truncal | SWC3 y SWC2 |  | f1/0 - p1



