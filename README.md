# Infraestrutura Ágil
## Pré-requisitos

Para utilizar este repositório você deverá instalar o [Vagrant](https://www.vagrantup.com/) e o [VirtualBox](https://www.virtualbox.org/).

Para clonar o repositório você precisará do [git](https://git-scm.com/), para os usuários do Windows recomendamos [https://gitforwindows.org/](https://gitforwindows.org/).

## Configuração

Nesse ambiente, que está centralizado no arquivo [Vagrantfile](https://github.com/4linux/525/blob/master/Vagrantfile), serão criados 5 máquinas com as seguintes características:

Nome            | vCPUs | Memoria RAM | IP            | S.O.         
----------------|:-----:|:-----------:|:-------------:|:---------------:
automation      | 2     | 2048MB      | 192.168.1.10  | debian/bullseye64
balancer        | 1     | 256MB       | 192.168.1.20  | debian/bullseye64
database        | 1     | 512MB       | 192.168.1.30  | centos-8.5
docker1         | 1     | 512MB       | 192.168.1.100 | debian/bullseye64
docker2         | 1     | 512MB       | 192.168.1.200 | centos-8.5


Clone o repositório em algum diretório da sua máquina e inicie as vms:

```bash
git clone https://github.com/4linux/4525.git
cd 4525
vagrant up
```

As máquinas serão provisionadas, este processo leva alguns minutos e depende da sua velocidade de conexão com a internet.

## Utilização

Todos os comandos devem ser utilizados dentro do diretório clonado.

Para listar as máquinas:

```bash
vagrant status
```

Para entrar em uma máquina:

```bash
vagrant ssh automation
```

Para iniciar as máquinas:

```bash
vagrant up
```

Para desligar as máquinas:

```bash
vagrant halt
```
