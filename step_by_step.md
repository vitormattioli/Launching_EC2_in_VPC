#### Objetivo 1: Criar uma VPC no console da aws.

Passo 1: 
* Logar no console da AWS
* Clicar em `Criar VPC`
* <img width="1399" alt="Captura de Tela 2023-10-23 às 22 03 22" src="https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/b863bd82-c79e-4ca8-9d2c-297e3ff6dbbf">

Na VPC são criados 2 subnets (publica e privada na sa-east-1a (dependendo da região que você configurou).

![Captura de Tela 2023-10-23 às 22 05 54](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/0fcff6b5-a344-42bc-ad20-8b19acec0606)

Além disso, são criadas 2 route tables (public and private). A route table publica pode ser usada pelas 2 subnets (publica e privada) e tem 2 privadas individuais que podem ser usadas pelas 2 subnets privadas anteriormente criadas.

![Captura de Tela 2023-10-23 às 22 06 17](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/374fc226-0f95-4424-a89c-b4789fa0e2f0)

### IPv4 CIDR Block

O /16 providencia 65k IPs
o tão sonhado /17 providencia 32k IPs
O /21 providencia 2k IPs
O /24 providencia 256 IPs (suficiente para esse passo a passo)
![Captura de Tela 2023-10-23 às 22 08 58](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/b495d1a7-cfac-4034-b08c-a8165939ac66)

![Captura de Tela 2023-10-23 às 22 10 46](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/5c16f5dc-6162-450d-bd82-438b51ca7183)


### Availability Zones.
é recomendado ter 2 AZs, mas para esse passo a passo podemos deixar só 1.
Numero de subnetes publicas: podemos deixar em 0, não vai fazer diferença para esse passo a passo.

![Captura de Tela 2023-10-23 às 22 13 09](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/e5fe38da-9d5e-45cf-9e76-3997b3593d49)


Com isso, clique em criar VPC.

o seu fluxo de trabalho será configurado

![Captura de Tela 2023-10-23 às 22 13 45](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/d1f5a990-ccc1-4b26-b858-f3c605293265
![Captura de Tela 2023-10-23 às 22 14 05](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/d11ed3b4-0fc4-4e94-aba9-a534f5a07e82)


#### Objetivo 2: Criar uma EC2

Passo 1:

* Clique em executar instancia, ou launch instance
* Defina um nome para a EC2, escolha a maquina, 
![Captura de Tela 2023-10-23 às 22 15 47](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/fd6b9fdc-29bc-41c5-9b8f-4ed90abea4df)
* Crie uma par de chaves (key pair)
  ![Captura de Tela 2023-10-23 às 22 17 08](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/64b647da-070e-4764-9b18-d25b1a273c67)
* Perceba que as configurações de rede já irão mostrar a VPC e a subnet
  Não é uma pratica recomendada deixar a porta 0.0.0.0/0 aberta, mas pra esse passo a passo ta de boa
![Captura de Tela 2023-10-23 às 22 18 02](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/3269cb55-e2a1-415f-8233-cbcc454abf1d)
* Clique em executar instancia
* ![Captura de Tela 2023-10-23 às 22 19 26](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/d2ed789f-8fbf-4179-9156-1191068b3f03)
* Perceba o ID da VPC dentro da sua EC2
* ![Captura de Tela 2023-10-23 às 22 19 57](https://github.com/vitormattioli/Launching_EC2_in_VPC/assets/86782203/3cc0a945-d60d-4159-9d1f-fa093a992cea)
* Encerre sua VPC e sua EC2 ;)\





