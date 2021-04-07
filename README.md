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

# Topologia1
![topo1](https://user-images.githubusercontent.com/53025349/113494603-fe7cb600-94a6-11eb-842d-2d8e5b45c276.jpg)


### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW8 y ESW9 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW9 y ESW10 | 2 enlaces | f1/3 - 4 |
| Po3 | Entre ESW8 y ESW10 | 2 enlaces | f1/5 - 6 |

# Topologia2

![unknown](https://user-images.githubusercontent.com/34359891/113498698-917c1700-94cc-11eb-944f-734a93393eda.png)

### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW1 y ESW2 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW1 y ESW3 | 3 enlaces | f1/3 - 5 |
| Po3 | Entre ESW1 y ESW4 | 3 enlaces | f1/6 - 8 |
| Po4 | Entre ESW2 y ESW3 | 3 enlaces | f1/9 - 11 |
| Po5 | Entre ESW2 y ESW4 | 3 enlaces | f1/12 - 14 |

# Topologia3
![topo3](https://github.com/jmansilla-2014056/galery/blob/master/Nueva%20carpeta/Topologia3.jpeg)

### EtherChannel
| EtherChanne | Entre | Enlaces | Puertos |
| ------------- | ------------- | ------------- | ------------- |
| Po1 | Entre ESW5 y ESW6 | 2 enlaces | f1/1 - 2 |
| Po2 | Entre ESW6 y ESW7 | 2 enlaces | f1/3 - 4 |
| Po3 | Entre ESW5 y ESW7 | 2 enlaces | f1/5 - 6 |
| Po4 | Entre ESW6 y ESW11 | 2 enlaces | f1/7 - 8 |
| truncal | SWC3 y SWC2 |  | f1/0 - p1


## VPN :blue_book:

Para conectar los 2 equipos con los que se realizo la practica, se utilizo el programa Open VPN, las direcciones y las llaves son generadas gracias a servicios de google cloud con una instacia ec2 y una regla de firewall. Basta con tener conexion y arrastrar el archivo (llave) al programa para configurar la VPN.

<div align='center'>
<img src="https://github.com/Stevensishernandez/RPV_PR1_1S2021/blob/main/image/OpenVpnMiguel.jpeg" width="35%" height="35%"/>
</div>

## Apache :green_book:

Los servicos de HTTP se montaron gracias a la ayuda de apache, regularmente todos los servicios son repartidos en sistemas operativos especiales para servidores pero en esta ocacion lo mas simple para levantar paginas es levantar servios con los host, la instalacion y utilizacion de apache en maquinas linux se resume en los siguientes comandos.
    
    sudo apt-get update
    sudo apt-get install apache2



