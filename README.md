Testes Caixa Cinza - API de Autenticação
Introdução

Este projeto foi desenvolvido como parte de uma atividade acadêmica sobre testes de caixa cinza em APIs de autenticação.

Foram utilizadas as ferramentas Supabase, Postman e GitHub para configurar um ambiente de autenticação, realizar requisições HTTP e validar o comportamento da API diante de diferentes situações.

Objetivo da Atividade

O objetivo desta atividade é compreender e aplicar testes de caixa cinza em APIs de autenticação, verificando o funcionamento do login, a validação de credenciais e as respostas retornadas pelo servidor.

Também tem como finalidade desenvolver conhecimentos sobre requisições HTTP, códigos de status, headers e respostas JSON.

Configuração do Supabase

Foi utilizado o Supabase para criar um ambiente de autenticação de usuários.

Primeiramente, foi criado um projeto na plataforma. Em seguida, foi habilitada a autenticação por e-mail e senha e cadastrado um usuário para realizar os testes.

Foram obtidas as seguintes informações:

Plataforma: Supabase
Tipo de autenticação: E-mail e senha
Nome do projeto: cavalheiro-will's Project
API URL: Configurada no ambiente do Postman
API Key: Chave pública do projeto

O objetivo dessa configuração foi disponibilizar uma API de autenticação para verificar o comportamento do sistema diante de credenciais válidas e inválidas.

Evidências

Os prints da configuração estão disponíveis na pasta prints/supabase/.

Configuração do Postman

Foi utilizado o Postman Desktop para executar as requisições HTTP.

Foi criado um Workspace chamado Testes API Supabase, utilizado para organizar as requisições.

Também foi criado um Environment chamado Supabase - Testes, contendo as seguintes variáveis:

Variável	Descrição
base_url	URL do projeto Supabase
api_key	Chave pública da API
email	E-mail do usuário cadastrado
password	Senha do usuário cadastrado

Essas variáveis facilitam a execução dos testes e permitem alterar os dados de autenticação sem modificar toda a requisição.

Configuração das Requisições

Foi criada uma requisição utilizando o método HTTP POST.

Endpoint utilizado:

/auth/v1/token?grant_type=password

URL completa:

{{base_url}}/auth/v1/token?grant_type=password

Headers utilizados
Header	Valor
apikey	{{api_key}}
Authorization	Bearer {{api_key}}
Content-Type	application/json
Body JSON
json
{
  "email": "{{email}}",
  "password": "{{password}}"
}


A requisição tem como finalidade verificar se as credenciais informadas pertencem a um usuário cadastrado e realizar sua autenticação.

Execução dos Testes

Foram definidos cinco cenários de testes para verificar o funcionamento da API.

Cenários executados
ID	Cenário	Entrada utilizada	Resultado esperado	Resultado obtido	Status
CT001	Login válido	E-mail e senha corretos	HTTP 200 e access token	[Preencher]	[Preencher]
CT002	Senha incorreta	E-mail correto e senha errada	Erro de autenticação	[Preencher]	[Preencher]
CT003	Usuário inexistente	E-mail não cadastrado	Acesso negado	[Preencher]	[Preencher]
CT004	Campos vazios	E-mail e senha vazios	Erro de validação	[Preencher]	[Preencher]
CT005	Credenciais inválidas	E-mail e senha inválidos	Mensagem de erro	[Preencher]	[Preencher]

Durante os testes foram analisados:

Códigos de status HTTP.
Respostas retornadas em JSON.
Mensagens de erro.
Retorno do access token.
Comportamento da autenticação.
Evidências

Os prints das execuções estão disponíveis na pasta prints/testes/.

Registro dos Testes

Os testes foram registrados em uma planilha Excel, contendo:

Identificação do teste.
Cenário.
Entrada utilizada.
Resultado esperado.
Resultado obtido.
Status.
Observações.

A planilha permite organizar os resultados e identificar possíveis falhas durante a execução.

Arquivo: planilha/registro-testes.xlsx.

Resultados Obtidos

Os resultados foram analisados após a execução das requisições no Postman.

Foram avaliados os códigos HTTP, as respostas JSON e as mensagens retornadas pela API.

Os resultados individuais de cada cenário estão registrados na tabela de execução dos testes e na planilha disponibilizada no repositório.

[Completar após executar todos os testes.]

Conclusão

A realização desta atividade permitiu compreender na prática o funcionamento de uma API de autenticação e a importância dos testes de caixa cinza.

Com o Supabase foi possível configurar um ambiente de autenticação por e-mail e senha. Por meio do Postman foram realizadas requisições HTTP para verificar o comportamento da API em diferentes cenários.

A atividade também possibilitou compreender a importância dos códigos de status HTTP, dos headers e das respostas JSON na validação de uma API.

Os testes contribuíram para identificar possíveis falhas de autenticação e verificar se o sistema responde corretamente diante de diferentes entradas.

[Adicionar as dificuldades encontradas e os resultados reais obtidos durante a atividade.]

Informações do Aluno
Aluno: [Seu nome]
Curso: [Seu curso]
Disciplina: [Nome da disciplina]
Professor: [Nome do professor]
Data: [Data da entrega]
