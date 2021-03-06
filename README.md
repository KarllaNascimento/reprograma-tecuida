<h1 align="center">
    <br>
    <p align="center">Projeto Final {reprograma}<p>
</h1>

<p align="center">
  <img width="470" src="src/assets/teCuida.gif">
</p>

## 1. Qual o problema? 

<br>

<p align="justify"> A sociedade capitalista, machista, racista e LGBTQIA+fóbica em que vivemos deu muito errado para a grande maioria das pessoas. O falso conservadorismo que nos permeia faz com que assuntos como a vida sexual da mulher não sejam discutidos. O resultado disso: violência. Se entre mulheres cis heterossexuais a experiência ginecológica já é traumática. Quando fazemos o recorte para mulheres lésbicas, bissexuais e pessoas não binárias, uma consulta ginecológica é composta por violência, apagamento, desrespeito e a sensação de que ter acesso ao básico, como um tratamento médico humanizado, é algo que jamais será alcançado. Afinal, o problema é bem mais profundo quando paramos para pensar que as faculdades de medicina não formam médicas e médicos para nada que não seja heteronormativo. 
  
<p align="justify"> Como resultado a esses dois problemas existe uma verdadeira fuga desse grupo das consultas ginecológicas. De acordo com a Febrasgo (Federação Brasileira das Associações de Ginecologia e Obstetrícia) 76% das mulheres (independentemente de sua sexualidade) realizam consultas ginecológicas anualmente. Mas quando falamos das mulheres que fazem sexo com mulheres o índice cai para 47%. Uma situação extremamente preocupante porque a prevenção é o melhor caminho para evitar problemas e ter uma boa saúde. 
  
<p align="justify"> Atualmente, o processo de encontrar ginecologistas que atendam mulheres lésbicas, bissexuais e pessoas não binárias sem discriminação e de maneira humanizada se dá por meio do boca a boca ou através de indicação em grupos nas redes sociais. Fora o difícil acesso para encontrar médicas/os especialistas para tratar sobre o assunto. Essas dificuldades tornam um processo que deveria ser natural em algo trabalhoso e cansativo.
    
[Fonte](https://portalarquivos2.saude.gov.br/images/pdf/2015/agosto/31/livreto-atencao-a-saude-de-mulheres-lesbicas-versao-web.pdf)
    
<br>    
    
## 2. O que propõe o projeto <strong>teCuida</strong>?     
    
<p align="justify"> Partindo do princípio que estamos no século XXI e que tamanho retrocesso é inaceitável, como forma de mitigar esse problema, inicialmente atendendo apenas o estado de Pernambuco, a <strong>teCuida</strong> busca ser um ambiente de referência capaz de criar uma base de médicas e médicos que realizam esse atendimento humanizado, assim como uma base para que essas/es médicas/os possam ter acesso a guias com instruções sobre como proceder corretamente em consultas e exames realizados em mulheres lésbicas, bissexuais e pessoas não binárias.
<br>
<br>
  
 ## 3. Como vai funcionar? 
  
<strong>teCuida</strong> é uma API RESTfull feita com a tecnologia Javascript no Node.js e integrada ao MongoDB que atende três clientes: usuáries, pessoas da medicina que buscam informação sobre o tema e especialistas atuantes na área desejam contribuir com seus conhecimentos. Sendo assim, será possível realizar ações como o cadastro, atualização e visualização de médicas/os que já fazem esse atendimento especializado, considerando informações como preço social, plano de saúde, descrição  do atendimento e gênero. Assim como também será possível, por parte das/os médicas/os atuantes, o cadastro e atualização de guias para realização de um atendimento não violento, pelo contrário! Que seja humanizado, atendendo as especificidades das mulheres cis e de pessoas não-binárias, independentemente de sua sexualidade. 

Por se tratar de um tema que requer cautela e abordagem segura, ações como cadastro, atualização e deleção de informações só podem ser realizadas por usuárias/os  já cadastradas/os no sistema.
<br>
<br>


## 4. Tecnologias utilizadas para a construção da API:
| Ferramenta | Descrição |
| --- | --- |
| `javascript` | Linguagem de programação. |
| `nodejs` | Runtime de JavaScript baseado no motor V8 JavaScript do Chrome.|
| `express` | Framework Node.js. |
| `MongoDb` | Banco de dado não relacional orietado a documentos.| 
| `npm ou yarn` | Gerenciador de pacotes.|
| `nodemon` | Dependência que monitora todas as alterações nos arquivos da aplicação e reinicia automaticamente o servidor sempre que for necessário.| 
| `cors` | Dependência que permite que um site acesse recursos de outro site mesmo estando em domínios diferentes.|     
| `bcrypt` | Biblioteca que adiciona um código aleatório ao hash original.|
| `mongoose` | Dependência que interage com o MongoDB para a conexão da database, criação do model e das collections.|
| `jsonwebtoken` | Dependência de autenticação entre duas partes por meio de um token assinado que autentica uma requisição web.|
| `dotenv` | Dependência para proteger dados sensíveis do projeto.|
| `MongoDb Compass` | Interface gráfica para verificar se os dados foram persistidos.|
| `Postman ou Insomnia` | Interface gráfica para realizar testes.|
| `MongoAtlas` | Serviço de DBaaS (Banco de Dados como Serviço) oferecido pela MongoDB.|
| `Heroku` | A Heroku é uma plataforma nuvem que faz deploy de várias aplicações back-end seja para hospedagem, testes em produção ou escalar as suas aplicações.|

<br>
<br>

## 5. 📁 Arquitetura MVC

```
 📁 teCuida
   |
   |-  📁 src
   |    |
   |    |- 📁 assets
   |    |    |- 📄 teCuida.gif
   |    |  
   |    |- 📁 controllers
   |    |    |- 📄 authController.js
   |    |    |- 📄 doctorUserController.js
   |    |    |- 📄 guideController.js
   |    |    |- 📄 userController.js 
   |    |
   |    |- 📁 data  
   |    |    |- 📄 dbConfig.js
   |    | 
   |    |- 📁 helpers
   |    |    |- 📄 check-token.js
   |    |    |- 📄 get-user-by-token.js
   |    |
   |    |- 📁 models
   |    |    |- 📄 doctorUser.js 
   |    |    |- 📄 guide.js 
   |    |    |- 📄 user.js
   |    | 
   |    |- 📁 routes
   |    |    |- 📄 auth.routes.js
   |    |    |- 📄 doctorUser.routes.js
   |    |    |- 📄 guide.routes.js
   |    |    |- 📄 index.js
   |    |    |- 📄 user.routes.js
   |    |   
   |    |- 📄 app.js 
   |    
   |- 📄 .env.example
   |- 📄 .gitignore
   |- 📄 package-lock.json
   |- 📄 package.json
   |- 📄 Procfile
   |- 📄 README.md 
   |- 📄 server.js

```

<br>
<br>

## 6. Documentação da API
    
### 6.1 [GET] "/" - Retorna um JSON com apresentação da API
    
```jsx
[
    {
    "título":"teCuida Api - Projeto final da {reprograma}",
    "version":"1.0.0",
    "mensagem":"Seja bem vinde! 🤖",
    "__v": 0
  }
]
```
### 6.2 Rota de criação e login de usuário

 Endpoint: {{URL}}api/auth  
    
| Rota | Método | O que faz |
| --- | --- | --- |
| `/resgister` | POST | Cadastro de usuário |
| `/login` | POST | Acesso do usuário a aplicação |
    
### 6.3 Rota de usuários  
 
 Endpoint: {{URL}}api/user   
    
 Rota | Método | O que faz |
| --- | --- | --- |
| `/user` | GET | Retorna todos os médicos/as cadastrados |
| `/user` | PUT | Atualiza cadastro do usuário | 
     
### 6.4 Rota CRUD para base de dados de médicas e médicos    
    
Endpoint: {{URL}}api/doctor 
    
 Rota | Método | O que faz |
| --- | --- | --- |
| `/create` | POST | Cadastro de médicas/os |
| `/all` | GET | Retorna médicas/os que aceitam plano de saúde |    
| `/healthPlan` | GET | Retorna médicas/os que aceitam plano de saúde |
| `/socialPrice` | GET | Retorna médicas/os que aceitam preço social |
| `/femaleGender` | GET | Retorna apenas médicas do gênero feminino |
| `/maleGender` | GET | Retorna apenas médicos do gênero masculino |
| `/update` | PUT | Atualiza cadastro de médicas/os através do id |
| `/:id` | DELETE | Deleta médicas/os cadastrados através do id |   
    
 ### 6.5 Rota CRUD para guia de orientações feitas por médicas/os especialistas
    
Endpoint: {{URL}}api/guide    
    
 Rota | Método | O que faz |
| --- | --- | --- |
| `/create` | POST | Cadastro de guia com orientações |
| `/allGuide` | GET | Retorna todas os guias de orientação |
| `/:id` | GET | Retorna guia de um/a médico/a específico pelo seu id |
| `/:id` | PATCH | Atualiza informações de um guia através do id |
| `/:id` | DELETE | Deleta um guia através do id | 
    
<br>
<br>
    
### 6.6 Schemas   
    
#### 6.6.1 Usuárias  
    
 ```jsx
[
name: {
      type: String
   },
   email: {
      type: String,
      required: true,
      match: /.+\@.+\..+/,
      unique: true
   },
   password: {
      type: String,
      required: true
   },
   doctor: {
      type: Boolean
   },
   crm: {
      type: Number
   }
]
```
#### 6.6.1 Médicas/os cadastrados pelas usuárias
    
 ```jsx
[
   name: {
      type: String,
      required: true
   },
   adress: {
      type: String,
      required: true
   },
   description: {
      type: String,
      required: true
   },
   feminineGender: {
      type: Boolean,
      required: true
   },
   socialPrice: {
      type: Boolean,
      required: true
   },
   healthPlan: {
      type: Boolean,
      required: true
   },
   userId: {
      type: mongoose.ObjectId
   },
   date: {
      type: Date,
      require: true,
      default: new Date
   }
]
```   
    
#### 6.6.1 Guias cadastrados pelas/os médicas/os
    
```jsx
[
   articles: {
      type: String,
      required: true
   },
   guidance: {
      type: String,
      required: true
   },
   approach: {
      type: String,
      required: true
   },
   userId: {
      type: mongoose.ObjectId
   },
   date: {
      type: Date,
      require: true,
      default: new Date
   }
]    
``` 
<br>
<br>
    
## 7. Regras de negócio 

#### Rota de registro:
    
- [x]  Cadastro só pode ser feito se todos os campos obrigatórios forem preenchidos;
- [x]  Cadastro só pode ser feitos se a senha digitada for a mesma da confirmação senha;
- [x]  Cadastro não pode ser aceito se o e-mail que já estiver no sistema;
- [x]  Ausência de CRM não pode ser impeditivo para realização de cadastro.
    
#### Rota de login:
    
- [x]  Acesso só pode ser liberado caso o e-mail e senha coincidam com os cadastrados anteriormente.
    
#### Rota de usuário:
    
- [x]  Atualização só pode ser feita por um usuário logado;
- [x]  Atualização de senha só acontece se as senhas coincidirem;
- [x]  Atualização só pode ser feita pelo próprio usuário.

#### Rota de cadastro de médicas/os:
    
- [x]  Cadastro só pode ser feito por um usuário logado;
- [x]  Nome, endereço, preço social, plano de saúde, descrição e gênero devem ser campos obrigatórios;
- [x]  O cadastro só pode ser realizado se todos os campos obrigatórios estiverem preenchidos;
- [x]  Cadastro duplicado não poderá ser aceito. 
    
#### Rota de visualização de médicas/os:    
- [x]  Deve ser possível retornar apenas médicas/os que aceitem preço social;
- [x]  Deve ser possível retornar apenas médicas/os que aceitem plano de saúde; 
- [x]  Deve ser possível retornar apenas médicas do gênero feminino; 
- [x]  Deve ser possível retornar apenas médicos do gênero masculino. 

    
#### Rota para atualização de médica/o:
    
- [x]  Atualização só pode ser feito por um usuário logado;
- [x]  A atualização só pode ser feita se todos os campos obrigatórios estiverem preenchidos.  
    
#### Rota para deletar médica/o: 

- [x]  Médico só pode ser apagado por um usuário logado no sistema.
    
#### Rota de cadastro de guia:
    
- [x]  Cadastro só pode ser feito por um usuário logado no sistema;
- [x]  Nome, endereço, preço social, plano de saúde, descrição e gênero devem ser campos obrigatórios;
- [x]  O cadastro só pode ser realizado se todos os campos obrigatórios estiverem preenchidos.
- [x]  O mesmo médico não pode ser cadastrado duas vezes.
    
#### Rota para atualização de guia:
    
- [x]  Atualização só pode ser feito por um usuário logado no sistema;
- [x]  A atualização só pode ser feita se todos os campos obrigatórios estiverem preenchidos. 
    
#### Rota para deletar guia:

- [x]  Guia só pode ser apagada por um usuário logado no sistema.    
    
<br>
<br>
    
## 8. Implementações Futuras

*  Desenvolvimento de uma interface gráfica;
*  Validação do CRM cadastrado pelos médicos especialistas;
*  Possibilidade de interação entre usuárias e médicos/as;
*  Criação de cadastro apenas com apresentação do CPF como forma de garantir a autenticidade da ausuária;
*  Possibilidade de usuárias contestarem informações cadastradas pelas/os médicas/os no guia;
* Ampliar o alcance para toda a região Nordeste e, posteriormente, o Brasil inteiro;
* Alcançar outros grupos que também façam parte da comunidade LGBTQIA+.    
    
<br>
<br>
    
## 9. Deseja contribuir?
    
1. Faça o download ou clone este repositório;
2. Abra seu Terminal/Prompt e navegue até o diretório reprograma-tecuida;
3. Rode: **$ npm install**;
1. Para subir o servidor é só rodar **$ npm run start**.
 
<br>
<br>
      
    
## 10. Autora :woman_technologist:     
     
  ### Karlla Nascimento
- [Instagram](https://www.instagram.com/karllanascimento/)
- [Linkedin](https://www.linkedin.com/in/karlla-nascimento/)
- [Github](https://github.com/KarllaNascimento)
- [Apresentação](https://www.canva.com/design/DAEj1inpg_A/U6vlO0nXIwr2yqIzG1keuA/view?utm_content=DAEj1inpg_A&utm_campaign=designshare&utm_medium=link&utm_source=homepage_design_menu)
    
    
    
    
