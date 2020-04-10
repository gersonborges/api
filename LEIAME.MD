API PLIXSITE 1.0
================

openapi: 3.0.0
# Added by API Auto Mocking Plugin
servers:
# Added by API Auto Mocking Plugin
# Added by API Auto Mocking Plugin
  - description: Plixisite API
    url: https://virtserver.swaggerhub.com/passupreto/plixsite/1.0.0
info:
  version: "1.0.0"
  title: PlixSite API OAuth2
  description: >-
    Esta API usa a autenticação OAuth2.
security:
  - accessCode:
      - read
      - write
paths:
  /autenticacao:
    post:
      summary: Autenticação do usuário
      description: >-
        Autenticação de usuário.
      responses:
        '200':
          description: OK
  /postos:
    get:
      summary: Lista os postos de gasolina
      description: >-
        Listagens dos postos de gasolina. Cada usuário vê os seus postos.
      security: []
      responses:
        '200':
          description: OK
    post:
      summary: Insere um novo postos de gasolina
      description: >-
        Inserçao de novo posto de gasolina. 
      security: []
      responses:
        '200':
          description: OK
  /postos/[123]:
    get:
      summary: Lista dados de um posto de gasolina de id 123
      description: >-
        Listagens dos dados de um postos de gasolina.
      security: []
      responses:
        '200':
          description: OK
    put:
      summary: Altera dados de um posto de gasolina de id 123
      description: >-
        Alteração dos dados de um posto de gasolina. 
      security: []
      responses:
        '200':
          description: OK
    delete:
      summary: Exclui um posto de gasolina de id 123
      description: >-
        Exclusão de um posto de gasolina. 
      security: []
      responses:
        '200':
          description: OK
components:
  schemas: {}
  securitySchemes:
    accessCode:
      type: oauth2
      flows:
        authorizationCode:
          authorizationUrl: 'http://plixsite.net/api/auth'
          tokenUrl: 'http://plixsite.net/api/token'
          scopes:
            write: possibilita a modificação de recursos
            read: possibilta a recuperação de recursos
  
  


  
