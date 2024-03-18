## 1. Découpage symétrique

Besoin max 50 equipements par service.

Nombre d'adresses disponilbes : 2^6 - 2 = 64

64 moins les 2 adresses (réseau et diffusion) = 62 adresses.

Nous pouvons adresse 62 machines par Pôle;, en notation CIDR /26



















|     | Adresse réseau | Adresse de broadcast | Adresse de début de plage | 	Adresse de fin de plage |
|   :---------: |  :-------: | :---------: |  :-------: | :-------: |
| Informatique | 172.16.1.0/26 |  172.16.1.63 | 172.16.1.1 | 172.16.1.62 |
|   DeV | 172.16.1.64/26 |  172.16.1.127 | 172.16.1.65 | 172.16.1.126 |
|   Admin | 172.16.1.128/26 |  172.16.1.191 | 172.16.1.129 | 172.16.1.190 |
|   Tech | 172.16.1.192/26 |  172.16.1.255 | 172.16.1.193 | 172.16.1.254 |


## 2. Découpage asymétrique

* Le Pôle informatique (50 équipements) --> 2^6 - 2 = 64 -2 = 62 adresses
* Le Pôle développement (12 équipements) --> 2^4 - 2 = 16 -2 = 14 adresses
* Le Pôle Administratif ( 20 équipements) --> 2^5 - 2 = 32 -2 = 30 adresses
* Le Pôle Technicien (15 équipements) --> 2^5 - 2 = 32 -2 30 adresses

|     | Adresse réseau | Adresse de broadcast | Adresse de début de plage | 	Adresse de fin de plage |
|   :---------: |  :-------: | :---------: |  :-------: | :-------: |
| Informatique | 172.16.1.0/26 |  172.16.1.63 | 172.16.1.1 | 172.16.1.62 |
|   DeV | 172.16.1.64/26 |  172.16.1.79 | 172.16.1.65 | 172.16.1.78 |
|   Admin | 172.16.1.80/26 |  172.16.1.111 | 172.16.1.81 | 172.16.1.110 |
|   Tech | 172.16.1.112/26 |  172.16.1.143 | 172.16.1.113 | 172.16.1.142 |
