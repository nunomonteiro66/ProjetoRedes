| Router                 | Ligado a          | Porta | IP                     |
| ---------------------- | ----------------- | ----- | ---------------------- |
| GigaPixLX              | GigaFxPorto       | g0/0  | 10.10.0.1/30           |
|                        | ISP_A_Lx          | g1/0  | 10.10.0.9/30           |
|                        | EMP_Y             | g2/0  | 10.10.0.13/30          |
|                        | ISP_B_Lx          | g3/0  | 10.10.0.5/30           |
| GigaFixPorto           | ISP_B_Porto       | g0/0  | 10.10.0.17/30          |
|                        | ISP_A_Porto       | g1/0  | 10.10.0.21/30          |
|                        | GigaPixLX         | g2/0  | 10.10.0.2/30           |
|                        |                   | s3/0  |                        |
| ISP_B_Lx               | GigaPixLX         | g0/0  | 10.10.0.6/30           |
|                        | Casa_A            | g1/0  | 10.1.0.1/30            |
|                        | Casa_B            | g2/0  | 10.1.0.5/30            |
| ISP_A_Lx               | GigaPixLX         | g1/0  | 10.10.0.10/30          |
|                        | Emp_X_Lx          | g2/0  | 10.0.0.1/30            |
|                        | ISP_A_Porto       | g0/0  | 10.0.0.5/30            |
| Emp_Y                  | GigaPixLX         | g0/0  | 10.10.0.14/30          |
|                        | www.wikipedia.org | g1/0  | 91.198.174.193/25 ???? |
|                        | wikimail.org      | g2/0  | 208.80.154.237/30      |
| ISP_B_Porto            | GigaFixPorto      | g0/0  | 10.10.0.18/30          |
|                        | DHCP              | g1/0  | 10.0.1.98/29 ???       |
|                        | DNS               | g2/0  | 10.0.8.7/28 ????       |
|                        | emailspb.pt       | g3/0  | 193.1.2.1/29 ????      |
|                        |                   |       |                        |
| ISP_A_Porto            | GigaFixPorto      | g1/0  | 10.10.0.22/30          |
|                        | ISP_A_Lx          | g0/0  | 10.0.0.6/30            |
|                        | Emp_X_Porto       | g3/0  | 10.0.0.9/30            |
| Casa_A                 | ISP_B_Lx          | g0/0  | 10.1.0.2/30            |
|                        | PC0               | f1/0  | 10.0.1.1/24            |
| Casa_B                 | ISP_B_Lx          | g0/0  | 10.1.0.6/30            |
|                        | PC1               | f0/0  | 10.0.2.1/24            |
| DHCP                   | ISP_B_Porto       | g0/0  | 10.0.1.99/29 ????      |
| DNS                    | ISP_B_Porto       | g0/0  | 10.0.8.8/28 ?????      |
| emailspb.pt            | ISP_B_Porto       | g0/0  | 193.1.2.3/29 ???       |
| Emp_X_Lx               | ISP_A_Lx          | g1/0  | 10.0.0.2/30            |
|                        | Switch0           | f0/0  | 172.0.0.1/7            |
| Emp_X_Porto            | ISP_A_Porto       | g0/0  | 10.0.0.10/30           |
|                        | Switch1           | f2/0  | 172.17.200.2/24        |
| www.wikipedia.org      | Emp_Y             | g0/0  | 91.198.174.192/25      |
| wikimail.org           | Emp_Y             | g0/0  | 208.80.154.238/30      |
| email.com              | RouterEmail       | g0/0  | 170.1.2.3/29 ???       |
| www.cnn.com            | RouterCNN         | g0/0  | 151.101.133.67/29 ??   |
| DNS 8.8.8.8            | RouterDNS         | g0/0  | 8.8.8.8/28 ??          |
| RouterEmail            | email.com         | g0/0  | 170.1.2.1/29 ???       |
| RouterCNN              | www.cnn.com       | g0/0  | 151.101.133.65/29 ??   |
| RouterDNS              | DNS 8.8.8.8       | g0/0  | 8.8.8.1/28 ??          |
| www.noticiascovilha.pt | Emp_X_Lx          | f0/0  | 173.249.51.18/7        |
| DHCP Lx                | Emp_X_Lx          | f0/0  | 172.16.0.1/30          |
| Intranet               | Emp_X_Porto       | f0/0  | 172.17.200.1/24        |
| DNS_Emp_X              | Emp_X_Porto       | f0/0  | 172.17.200.3/24        |



# VLAN

| Switch  | VLAN       | Portas | IP - Router         |
| ------- | ---------- | ------ | ------------------- |
| Switch0 | VLAN - 100 | 2-10   | 172.16.100.1/24     |
|         | VLAN - 101 | 11-15  | 172.16.101.1/24     |
|         | VLAN - 1   | 16-20  | 172.16.1.1/24       |
|         | VLAN - 99  | 21-24  | 172.16.99.1/24      |
|         | VLAN - 102 | 17     | 172.16.0.2/30       |
| Switch1 | VLAN - 1   | 2-10   | 172.17.1.1/24       |
|         | VLAN - 100 | 11-15  | 172.17.100.1/24     |
|         | VLAN - 101 | 16-20  | 172.17.101.1/24     |
|         | VLAN - 200 | 21-24  | 172.17.128.1/17 ??? |




> Nota: p.e: 10.10.0.0 é a network, 10.10.0.1 e .2 sao os ip's disponiveis para os pc (neste caso routers) e 10.10.0.3 é o endereco de broadcast. Logo, para cada 2 ligaçoes é necessário "saltar" 4 ip's

> Nota2: salvar configuracoes dos routers todos

> Nota3: servidor/router com diferentes submasks ????

> Nota4: salvar todas as configuracoes dos routers/switches?? no final



| Router    | Porta | Subnet       | IP Router     | IP Subnet     | Rota de sumarização |
| --------- | ----- | ------------ | ------------- | ------------- | ------------------- |
| Emp_X_Lx  | f0/0  | Switch0      |               |               | 172.16.0.0          |
|           | g1/0  | ISP_A_Lx     |               |               | 10.0.0.0            |
| ISP_A_Lx  | g2/0  | Emp_X_Lx     |               |               | 10.0.0.0            |
|           | g1/0  | GigaPixLX    |               |               | 10.10.0.8           |
|           | g0/0  | ISP_A_Porto  |               |               | 10.0.0.4            |
| GigaPixLx | g1/0  | ISP_A_Lx     | 10.10.0.9/30  | 10.10.0.10/30 | 10.10.0.8           |
|           | g0/0  | GigaFixPorto | 10.10.0.1/30  | 10.10.0.2/30  | 10.10.0.0           |
|           | g2/0  | Emp_Y        | 10.10.0.13/30 | 10.10.0.14/30 | 10.10.0.12          |
|           | g3/0  | ISP_B_Lx     | 10.10.0.5/30  | 10.10.0.6/30  | 10.10.0.4           |

| Router       | Ligado a          | Porta | IP Router         | IP Subnet     | Rota de sumarizacao |      |
| ------------ | ----------------- | ----- | ----------------- | ------------- | ------------------- | ---- |
| GigaFixPorto | ISP_B_Porto       | g0/0  | 10.10.0.17/30     | 10.10.0.18/30 | 10.10.0.16          |      |
|              | ISP_A_Porto       | g1/0  | 10.10.0.21/30     | 10.10.0.22/30 | 10.10.0.20          |      |
|              | GigaPixLX         | g2/0  | 10.10.0.2/30      | 10.10.0.1/30  | 10.10.0.0           |      |
|              |                   | s3/0  |                   |               |                     |      |
| ISP_B_Lx     | GigaPixLX         | g0/0  | 10.10.0.10/30     |               |                     |      |
|              | Casa_A            | g1/0  | 10.0.0.1/30       |               |                     |      |
|              | Casa_B            | g2/0  | 10.0.0.5/30       |               |                     |      |
| Emp_Y        | GigaPixLX         | g0/0  | 10.10.0.14/30     |               |                     |      |
|              | www.wikipedia.org | g1/0  | 91.198.174.193/25 |               |                     |      |
|              | wikimail.org      | g2/0  | 208.80.154.237/30 |               |                     |      |
| ISP_B_Porto  | GigaFixPorto      | g0/0  | 10.10.0.18/30     | 10.10.0.17/30 | 10.10.0.16          |      |
|              | DHCP              | g1/0  | 10.0.1.98/29      |               |                     |      |
|              | DNS               | g2/0  | 10.0.8.7/28       |               |                     |      |
|              | emailspb.pt       | g3/0  | 193.1.2.1/29      |               |                     |      |
| ISP_A_Porto  | GigaFixPorto      | g1/0  | 10.10.0.22/30     |               |                     |      |
|              | ISP_A_Lx          | g0/0  | 10.0.0.6/30       |               |                     |      |
|              | Emp_X_Porto       | g3/0  | 10.0.0.9/30       |               |                     |      |
| Emp_X_Porto  | ISP_A_Porto       | g0/0  | 10.0.0.10/30      |               |                     |      |
|              | Switch1           | f2/0  | 172.17.200.2/24   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |
|              |                   |       |                   |               |                     |      |

