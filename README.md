## 📚 Seções Portfólios

<h4 align="left"><a href="https://github.com/caroolps/Portfolio01">PROJETO 1º SEMESTRE: Mapeador de Criminalidade ao Redor da FATEC</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio02">PROJETO 2º SEMESTRE: Gantt Chart</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio03">PROJETO 3º SEMESTRE: Cadastro Positivo</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio04">PROJETO 4º SEMESTRE: JobNation</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio05">PROJETO 5º SEMESTRE: Educalytics</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio06">PROJETO 6º SEMESTRE: Opt-In/Out</a></h4>

![image](https://user-images.githubusercontent.com/61089745/158082449-894548ea-e14d-4de7-896d-12d2a9ec1d74.png)

## FATEC 2022 - OPTIN/OPTOUT:anchor:

### **I - RESUMO DO PROJETO**:page_facing_up: 
A loja de esporte "FTSports" para atender a Lei geral da proteção de dados (LGPD), precisa se adequadar a modalidade optIn - optOut, concedendo poder ao cliente em permitir que manipule suas preferências de configurações. Com isso, a loja precisa adequar sua plataforma para que o usuário consiga alterar suas preferências de receber sms, whatsapp ou ligações de ofertas da loja a qualquer momento. E para segurança, todas essas alterações devem ser registradas no banco de dados.

### PROPOSTA
O projeto tem como objetivo atender a LGPD (Lei geral da proteção de dados), apresentando uma solução de configurações de meios de comunicação que um determinado usuário tem o poder de receber ou deixar de receber algumas informações da plataforma, ou seja, OptIn- OptOut. Contudo, a cada alteração nas permissões opt in-out devem ser apresentadas em uma tabela de histórico, descrevendo qual a versão do termo aceitado pelo usuário no momento do seu registro no sistema, e quais foram as opções aceitas, ou não no momento em que este usuário se registrou ou fez alguma alteração em seus dados posteriormente.

### REGRAS DO PROJETO
- Na criação ou alteração do cadastro do usuário irá gerar um registro na tabela Histórico;
- O termo ativo será o último cadastrado no banco de dados com seus detalhes de versão e data de criação;
- Usuário tem o poder de permitir ou não receber sms, ligações e whats de ofertas do sistema;
- No momento da criação ou edição do usuário, é necessário passar a versão do termo que ele está aceitando e registrar na tabela de histórico;
- Dentro do histórico será possível identificar o usuário, suas novas configurações optIn - optOut e qual a versão aceita pelo usuário.

### ENDPOINTS

## Termo
### Criar termo

Endpoint responsável por criar um termo.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161169371-f0968594-7d3c-4a18-a73b-34a48ef07cc7.png)


### Get All
Pega todos os termos.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161169527-5d588983-018f-4909-86e3-443b67476154.png)



### Get By id
Pega um termo por id.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161169580-90e5e693-2fb5-4bc4-a15d-2bf15e81e297.png)

### Get latest
Pega o termo mais recente.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161169655-240bf95c-2caa-4e12-b5da-661a7b7eea47.png)

##  Usuário
### Criar usuário

**Funcionamento** 

Criando usuário sem informar termo:

![image](https://user-images.githubusercontent.com/61089745/161170350-f8865600-9800-448d-b1db-3170c0cc04d0.png)

Criando usuário com termo antigo:

![image](https://user-images.githubusercontent.com/61089745/161170416-979cbaec-c178-4d60-a2ca-ecde89c839ba.png)

Criando usuário:

![image](https://user-images.githubusercontent.com/61089745/161170480-dbc56e30-a3e5-47da-be41-757dc769eced.png)

### Atualizar usuário
**Funcionamento**

Atualizar com termo inválido:

![image](https://user-images.githubusercontent.com/61089745/161170601-d0dc452f-e086-4b80-9cc6-2091a02ef9d4.png)

### Pegar as configs do usuario
Pega as configs de um usuário.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161170800-2e2a26de-c29d-4931-ab29-247839bc5c7f.png)

### Pegar termo do usuário
Pega o termo aceito pelo usuário.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161170851-c22247a3-b27f-4f60-9844-24a8a4c049e8.png)


## Histórico

### Pegar todos históricos
Pega todos os históricos.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161170955-6717d348-2d44-4bf4-8fcc-ea1ac64fcb3f.png)

### Pegar histórico por id
Pega um histórico por id.

**Funcionamento:**

![image](https://user-images.githubusercontent.com/61089745/161171013-847f8523-13e1-478a-8590-9a3da05bf4eb.png)


### Pegar histórico por usuário

**Funcionameto:**

![image](https://user-images.githubusercontent.com/61089745/161171097-b097280a-2ecc-4ac3-874d-ef6c08a63442.png)

### Histórico pelo termo

**Funcionameto:**

![image](https://user-images.githubusercontent.com/61089745/161171178-ef3037b8-e834-4f02-a24b-100486a07dcb.png)

### Histórico por sms
Pega todos os históricos com sms ativo.

**Funcionameto:**

![image](https://user-images.githubusercontent.com/61089745/161171387-4078c2e6-ade8-4266-90f2-563df6471a2b.png)

### Histórico pelo whats
Pega todos os históricos com whats.

**Funcionameto:**

![image](https://user-images.githubusercontent.com/61089745/161171450-428e7242-bace-4027-a553-1e895a089537.png)

### Histórico por ligacao

Pega todos os históricos com ligacao ativo.

**Funcionameto:**

![image](https://user-images.githubusercontent.com/61089745/161171518-6b20b9b6-9c6f-43bb-b09f-f29296a2639a.png)

### **II - TECNOLOGIAS**:iphone:

![image](https://user-images.githubusercontent.com/61089745/164816460-6561ae44-68de-4faf-99a7-299122107672.png)

JAVA: É uma linguagem de programação orientada a objetos. Foi utilizado essa linguagem para o desenvolvimento do backend da aplicação.

![image](https://user-images.githubusercontent.com/61089745/164816514-ea5b1677-1816-414e-874b-09e0c6975cce.png)

ECLIPSE: Java é uma linguagem de programação orientada a objetos, para desenvolver o backend foi usado o ambiente Eclipse para desenvolvimento integrado, escrito em Java.

![image](https://user-images.githubusercontent.com/61089745/164816585-ecd79b2f-43ff-45ac-ab36-0ee5eee8eef5.png)

MySQL: O MySQL é um sistema de gerenciamento de banco de dados, que utiliza a linguagem SQL como interface. Foi usado para o desenvolvimento do banco relacional da aplicação.

![image](https://user-images.githubusercontent.com/61089745/164816549-d7b2f5fe-86fe-430c-bbc3-172a22257bb2.png)

INSOMNIA: É um API Client que facilita aos desenvolvedores criar, compartilhar, testar e documentar APIs. Utizada para testar o GET, PUT, POST e DELETE das classes controllers da aplicação.

### **III - CONTRIBUIÇÕES INDIVIDUAIS**:bow:

Desenvolvimento do backend com as entidades e todas as camadas da aplicação

Conexão com o Banco de Dados MySQL pelo arquivo properties

Requisições VIA INSOMNIA


### **IV - APRENDIZADOS EFETIVOS**:closed_book:

**Hard Skills Efetivamente Desenvolvidas:**
Aperfeiçoamento no backend
ENUMS
MySQL
OPT-In/Out
Modelar o banco de dados
Realizar requisições
Regra de negócio

**Soft Skills Efetivamente Desenvolvidas:**
Tive a capacidade de planejar o escopo do projeto, determinando por onde iniciar, definindo data de entrega
Resiliência para construir todo o backend do projeto
AutoConfiança para determinar que sou capaz de desenvolver uma aplicação sozinha




