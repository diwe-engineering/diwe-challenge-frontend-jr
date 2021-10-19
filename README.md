

  

# Dev Froned Pleno - Desafio

  

### O candidato deverá desenvolver um crud de contatos com autenticação, abaixo os requisitos de sistema.

## STACK

  

1. HTML

  

3. CSS

  

4. JS com Vuejs ( SPA com router e vuex )

  

## ESPECIFICAÇÕES

  

1. Visualmente deverá estilizar seus elementos utilizando css puro ( sem frameworks como bootstrap ou tailwind), lembrando que a utilização de flexbox e elementos responsivos serão considerados diferenciais e deve seguir fielmente o layout proposto: 
**Link do layout ( figma ) :** https://www.figma.com/file/MlDF7BP1BgodRv0BO4EQ4C/Desafio?node-id=2%3A1694.

  

2. O Software deverá conter uma página de login que irá autenticar o sistema com um token JWT enviado pela api;

  

3. Deverá também, conter telas com todas as operações de um crud (Create, Read, Update, Delete) e estas deverão ser acessadas somente se a sessão estiver autenticada com um token válido.



## REQUISITOS

Os cadastros de contato devem conter 3 campos, sendo eles
1. campo obrigatório nomeado name (String de no máximo 200 carácteres)
2. campo obrigatório nomeado email (String de máximo 200 carácteres contendo obrigatório nomeado válido não necessariamente existente) 
3. campo required mobile (Interger de no máximo 11 carácteres)

O formulário deve ter tratativa de erro, sendo assim em caso de algum erro com o servidor uma mensagem tratada deve ser apresentada

## API PARA INTEGRAÇÃO

Autenticação
```
POST
https://testfrontpl.herokuapp.com/login

body:

{
    "user": "devfrontpl@diwe.com.br",
    "pwd": "frontPl@2021"
}
```

Todas as demais rotas precisam receber o token como header.
```
HEADER
content-type: appllication-json
x-access-token: token retornado pela signin
```

Criar Cliente
```
POST
https://testfrontpl.herokuapp.com/clientes

{
    "name": "nome_do_cliente",
    "email": "email_do_cliente",
    "mobile": "telefone_do_cliente"
}
```

Listar todos os cliente
```
GET
https://testfrontpl.herokuapp.com/clientes
```

Detalhes do cliente
```
GET
https://testfrontpl.herokuapp.com/clientes/:id
```

Update de cliente
```
PUT
https://testfrontpl.herokuapp.com/clientes/:id

{
    "name": "nome_do_cliente",
    "email": "email_do_cliente",
    "mobile": "telefone_do_cliente"
}
```

Excluir Cliente
```
DELETE
https://testfrontpl.herokuapp.com/clientes/:id
```


### Para envio do teste:

  

  

1. Deverá ser criado um repositório no git ou bitbucket com o nome de Test-Dev-Front-PL. Esse repositório deverá conter todo o código desenvolvido.

  

2. Enviar o link do repositório para os emails de Paulo Tozzi (paulo.tozzi@diwe.com.br), Vinicius Silva (vinicius.silva@diwe.com.br) e Maicon Passos (maicon.passos@diwe.com.br)
