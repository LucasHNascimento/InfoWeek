# InfoWeek

REST

um acronimo para Representational State Transfer (Transferencia de Estado Representativo)

A transferencia de dados de uma meneira figurativa, representativa e de maneira didatica.

A transferencia de dados, geralmente, é realizada usando protocolo HTTP

O Rest delimita obrigações para nesses transferencia de dados

Resource seria então uma entidade ou um objeto.

Request/Response

### NECESSIDADES (CONSTRAINTS) para ser RestFul

_Uniform Interface_: Manter uma uniformidade, ou uma constancia, e ou padrão para a construção desta interface. A nossa API tem que ser coerente com quem vai consumi-la. Usar somente uma linguagem de comunicação (JSON) e não varias ao mesmo tempo. Sempre enviar respostas aos clientes;

_Cliente server_: Separação do cliente e do armazenamento de dados (servidor), dessa forma, poderemos ter portabilidade entre os cliente como react-native (mobile) ou por exemplo react (web).

_Statelees_: Cada requisição que o cliente faz para o servidor, deverá conter as informações necessárias para o servidor entender e responder (Response) e a Requisição (Request). Exemplo: A sessão do usuário devera ser enviada para todas as requisições, e o servidor não pode lembrar que o cliente foi autenticado na requisição anterior. Nós no portal por exemplo, temos por padrão que usar tokens para as comunicações.

_Cacheable_: As respostas para uma requisição, deverão ser explicitas ao dizer se aquela requisição, pode ou não ser cacheada pelo cliente.

_Layered System_: O cliente acessa a um endpoint, sem precisar saber da complexidade, de quais passos estão sendo necessários para o servidor responder a requisição.

_Code on demanda (optnal)_: Da a possibilidade da nossa aplicação (API) pegar códigos, como o javascript, o executar no cliente.

## RestFul

Restful é a aplicação de todos os padrões REST

## BOAS PRATICAS

- Utilizar verbos HTTP para nossas requisições
- Utilizar plural ou singular na criação de endoints (Isso importa)
- Não deixe bara final no seu endpoint (/Cliente/)
- Nunca deixe o cliente sem resposta

## VERBOS HTTP

- GET: Receber dados de um Resource
- POST: Enviar dados ou info para serem processados por um Resource
- PUT: Atualizar dados de um Resource
- DELETE: Deletar um Resource

## STATUS DAS RESPOSTAS (RESPONSES)

- 1XX: Informação
- 2XX: Sucesso
    - 200: OK
    - 201: CREATED
    - 204: Não tem conteúdo PUT POST DELETE
- 3XX: Redirection
- 4XX: Clent Error
    - 400: Bad Request
    - 404: Not Found!
- 5XX: Server Error
    - 500: Internal Server Error