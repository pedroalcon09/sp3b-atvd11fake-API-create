### Fake API usage:

## Routes:

> POST /register --> não precisa de permissão para cadastrar novos usuários no banco
> POST /login --> endpoint para fazer login e obter o token para permissões
> GET /users/:userId --> precisa de permissão para ler os usuários existentes

> POST /albuns --> Usuário precisa de permissão pra posta um novo álbum
> GET /albuns --> todos podem ver os albuns cadastrados
> GET /albuns/:id --> todos podem ver o albun cadastrados com id especificado

> POST /foods --> não é possível escrever nesse endpoint
> GET /foods --> usuário precisa de permissão para ler infos

## Permissão:

> Para rotas que precisam de permissão:

header : {
Authorization: Bearer token
}

> O token pode ser obtido ao fazer um registro ou um login pelas rotas /users.A chave que esta na chave "accessToken" deve ser colocada sem aspas onde esta o token na orientação a cima.

## Formatação:

> Foods :
> {

      "name": "Name",
      "price": Number,
      "color": "color"
    }

> Albuns :
> {

      "name": "Album name",
      "id": number,
      "band": "Composer",
      "year": Year(number)
    }

> Users :
> {

      "email": "example@email.com",
      "password": "password",
      "id": number
    }
