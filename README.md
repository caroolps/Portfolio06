## 📚 Seções Portfólios

<h4 align="left"><a href="https://github.com/caroolps/Portfolio01">PROJETO 1º SEMESTRE: Mapeador de Criminalidade ao Redor da FATEC</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio02">PROJETO 2º SEMESTRE: Gantt Chart</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio03">PROJETO 3º SEMESTRE: Cadastro Positivo</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio04">PROJETO 4º SEMESTRE: JobNation</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio05">PROJETO 5º SEMESTRE: Educalytics</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/Portfolio06">PROJETO 6º SEMESTRE: Opt-In/Out</a></h4>

![image](https://user-images.githubusercontent.com/61089745/158082449-894548ea-e14d-4de7-896d-12d2a9ec1d74.png)

## Projeto de Tópicos avançados de banco de dados - Banco de dados - FATEC 2022 - OPTIN/OPTOUT:mortar_board:

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

Endpoint responsavel por criar um termo

**Path**
```
POST <host>/spring-app/termo/new
``` 

**Request** 
```
curl --request POST \
  --url http://localhost:8081/spring-app/termo/new \
  --header 'content-type: application/json' \
  --data '{
	"nome": "Terceiro termo",
	"conteudo": "O super conteudo do meu terceiro termo",
	"versao": "2"
}'
```

**Funcionamento**
![image](https://user-images.githubusercontent.com/61089745/161169371-f0968594-7d3c-4a18-a73b-34a48ef07cc7.png)


### Get All
Pega todos os termos

**Path**
```
GET <host>/spring-app/termo/all
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/termo/all
```
**Funcionamento**
![image](https://user-images.githubusercontent.com/61089745/161169527-5d588983-018f-4909-86e3-443b67476154.png)



### Get By id
Pega um termo por id

**Path**
```
GET <host>/spring-app/termo/<id_termo>
``` 


**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/termo/1
```

**Funcionamento**
![image](https://user-images.githubusercontent.com/61089745/161169580-90e5e693-2fb5-4bc4-a15d-2bf15e81e297.png)

### Get latest
Pega o termo mais recente
**Path**
```
GET <host>/spring-app/termo
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/termo/
```

**Funcionamento**

![image](https://user-images.githubusercontent.com/61089745/161169655-240bf95c-2caa-4e12-b5da-661a7b7eea47.png)

##  Usuário

### Criar usuario
Cria um usuario

**Path**
```
POST <host>/spring-app/usuario/new
``` 
**Request**
```
curl --request POST \
  --url http://localhost:8081/spring-app/usuario/new \
  --header 'content-type: application/json' \
  --data '{
	"nome": "super usuario",
	"email": "superemai@email.com",
	"cpf": "12312312312",
	"celular": "5512912345678",
	"rua": "super rua",
	"numero": "super numero",
  "bairro": "super bairro",
	"cidade": "super cidade",
	"cep": "12345678",
	"sms": 0,
	"whats": 0,
	"ligacao": 0,
	"termoVersao": 1
}'
```

**Funcionamento**

Criando usuario sem informar termo

![image](https://user-images.githubusercontent.com/61089745/161170350-f8865600-9800-448d-b1db-3170c0cc04d0.png)

Criando usuario com termo antigo

![image](https://user-images.githubusercontent.com/61089745/161170416-979cbaec-c178-4d60-a2ca-ecde89c839ba.png)

Criando usuario

![image](https://user-images.githubusercontent.com/61089745/161170480-dbc56e30-a3e5-47da-be41-757dc769eced.png)

### Atualizar usuario
Atualiza um usuario

**Path**
```
PUT <host>/spring-app/usuario/edit
``` 

**Request**

```
curl --request PUT \
  --url http://localhost:8081/spring-app/usuario/edit \
  --header 'content-type: application/json' \
  --data '{
	"id": 1,
	"nome": "super usuario",
	"email": "superemai@email.com",
	"cpf": "12312312312",
	"celular": "5512912345678",
	"rua": "super rua",
	"numero": "super numero",
  "bairro": "super bairro",
	"cidade": "super cidade",
	"cep": "12345678",
	"sms": 2.0,
	"whats": 2.0,
	"ligacao": 2.0,
	"termoVersao": 3
}'
```


**Funcionamento**

Atualizar com termo invalido
![image](https://user-images.githubusercontent.com/61089745/161170601-d0dc452f-e086-4b80-9cc6-2091a02ef9d4.png)

### Pegar as configs do usuario
Pega as configs de um usuario

**Path**
```
GET <host>/spring-app/usuario/config/<id_usuario>
``` 
**Request**

```
curl --request GET \
  --url http://localhost:8081/spring-app/usuario/config/1
```

**Funcionamento**

![image](https://user-images.githubusercontent.com/61089745/161170800-2e2a26de-c29d-4931-ab29-247839bc5c7f.png)

### Pegar termo do usuario
Pega o termo aceito pelo usuario

**Path**
```
GET <host>/spring-app/usuario/termo/<id_usuario>
``` 

**Request**

```
curl --request GET \
  --url http://localhost:8081/spring-app/usuario/termo/1
```

**Funcionamento**

![image](https://user-images.githubusercontent.com/61089745/161170851-c22247a3-b27f-4f60-9844-24a8a4c049e8.png)


## Historico

### Pegar todos historicos
Pega todos os historicos

**Path**
```
GET <host>/spring-app/historico/all
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/historico/all
```

**Funcionamento**

![image](https://user-images.githubusercontent.com/61089745/161170955-6717d348-2d44-4bf4-8fcc-ea1ac64fcb3f.png)
Em
### Pegar historico por id
Pega um historico por id

**Path**
```
GET <host>/spring-app/historico/<id_historico>
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/historico/4
```

**Funcionamento**

![image](https://user-images.githubusercontent.com/61089745/161171013-847f8523-13e1-478a-8590-9a3da05bf4eb.png)


### Pegar historico por usuario

**Path**
```
GET <host>/spring-app/historico/usuario/<id_usuario>
``` 
**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/historico/usuario/1
```

**Funcionameto**
![image](https://user-images.githubusercontent.com/61089745/161171097-b097280a-2ecc-4ac3-874d-ef6c08a63442.png)

### Historico pelo termo

**Path**
```
GET <host>/spring-app/historico/termo/<id_termo>
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/historico/termo/3
```

**Funcionameto**
![image](https://user-images.githubusercontent.com/61089745/161171178-ef3037b8-e834-4f02-a24b-100486a07dcb.png)

### Historico por sms
Pega todos os historicos com sms ativo


**Path**
```
GET <host>/spring-app/historico/sms/<valor>
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/historico/sms/2
```

**Funcionameto**
![image](https://user-images.githubusercontent.com/61089745/161171387-4078c2e6-ade8-4266-90f2-563df6471a2b.png)

### Histórico pelo whats
Pega todos os historicos com whats

**Path**
```
GET <host>/spring-app/historico/whats/<valor>
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/historico/whats/2
```

**Funcionameto**
![image](https://user-images.githubusercontent.com/61089745/161171450-428e7242-bace-4027-a553-1e895a089537.png)

### Historico por ligacao

Pega todos os historicos com ligacao ativo

**Path**
```
GET <host>/spring-app/historico/ligacao/<valor>
``` 

**Request**
```
curl --request GET \
  --url http://localhost:8081/spring-app/historico/ligacao/2
```

**Funcionameto**
![image](https://user-images.githubusercontent.com/61089745/161171518-6b20b9b6-9c6f-43bb-b09f-f29296a2639a.png)

