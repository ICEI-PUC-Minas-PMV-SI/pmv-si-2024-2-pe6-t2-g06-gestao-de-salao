# GESTÃO DE SALÃO

`CURSO: Sistemas de Informação`

`DISCIPLINA: Projeto - Arquitetura de Sistemas Distribuídos`

`SEMESTRE: 6º`

A proposta do projeto "Gestão de Salão" é criar um aplicativo mobile que melhore a experiência do cliente e atenda as necessidades em relação ao relacionamento com salões. 
Com ele, os clientes podem efetuar um cadastro único, agendar horários e até mesmo utilizar códigos QR para acessar promoções exclusivas e facilitar o check-in. Tudo isso diretamente pelo smartphone, proporcionando uma experiência personalizada e simplificada, que economiza tempo e melhora a interação com os serviços oferecidos. 

## Integrantes

* Everton de Souza Kenedy
* Lucas Marcio Nascimento Costa Lima
* Roberto Santos de Almeida
* Sara Vidal de Souza
* Sarah Moura Miranda

## Orientador

* Kleber Jacques Ferreira de Souza

# Planejamento

| Etapa         | Atividades |
|  :----:   | ----------- |
| ETAPA 1         |[Documentação de Contexto](docs/contexto.md) <br> |
| ETAPA 2         |[Planejar, desenvolver e gerenciar APIs e Web Services](docs/backend-apis.md) <br> |
| ETAPA 3         |[Planejar, desenvolver e gerenciar uma aplicação Web](docs/frontend-web.md) |
| ETAPA 4        |[Planejar, desenvolver e gerenciar uma aplicação Móvel](docs/frontend-mobile.md) <br>  |
| ETAPA 5         | [Apresentação](presentation/README.md) |
## Instruções de utilização

Assim que a primeira versão do sistema estiver disponível, deverá complementar com as instruções de utilização. Descreva como instalar eventuais dependências e como executar a aplicação.

## Requisitos Não Funcionais

| *Categoria*      | *Descrição*                                                                                                                                                                      |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Desempenho*     | *Tempo de Resposta*: A aplicação deve carregar as principais funcionalidades, como login e seleção de serviços, em até 1 segundo, idealmente medido em milissegundos.             |
|                    | *Escalabilidade*: O sistema deve suportar entre 20 a 100 acessos simultâneos sem perda significativa de desempenho.                                                              |
|                    | *Capacidade de Processamento*: A aplicação deve ser capaz de processar múltiplas requisições simultâneas, especialmente durante horários de pico, sem afetar a performance.       |
| *Usabilidade*    | *Interface Amigável*: A interface deve ser intuitiva e otimizada para dispositivos móveis, facilitando o acesso a informações e a navegação entre as páginas de cadastro, escolha de serviços e agendamento. |
|                    | *Compatibilidade com Dispositivos Móveis*: A aplicação deve ser responsiva e garantir uma excelente experiência em dispositivos móveis, incluindo smartphones e tablets que utilizem Android e iOS. |
|                    | *Documentação Básica*: Incluir uma breve documentação ou tutorial que ajude os usuários a entender como usar a aplicação.                                                         |
| *Segurança*      | *Autenticação*: Implementar autenticação básica, garantindo que apenas pessoas autorizadas possam acessar ou modificar informações.                                                |
|                    | *Hashing Simples*: Implementar hashing para senhas utilizando um algoritmo de pelo menos 256 bits para garantir a segurança.                                                     |
|                    | *Proteção de Dados Pessoais*: Armazenar dados pessoais dos usuários de forma segura, utilizando o hashing de senhas especificado acima.                                           |
| *Confiabilidade* | *Backup Semanal*: Realizar backups semanais dos dados críticos. Nos bastidores, o backup deve ser automatizado para garantir a segurança e a recuperação dos dados.               |
|                    | *Estabilidade Básica*: A aplicação deve funcionar de forma estável durante as demonstrações e testes, sem quedas frequentes.                                                     |
| *Maneabilidade*  | *Código Limpo e Bem Comentado*: Esta prática é recomendada, mas não é um requisito não funcional. Garantir um código organizado e comentado facilita a manutenção e a compreensão por outros desenvolvedores. |
| *Portabilidade*  | *Compatibilidade com Sistemas Operacionais*: A aplicação deve ser compatível com dispositivos móveis rodando Android e iOS.                                                      |
| *Escalabilidade* | *Suporte para Usuários Simultâneos*: O sistema deve suportar de 20 a 100 acessos simultâneos sem perda de performance, permitindo uma escalabilidade básica adequada ao contexto de demonstração. |

# Código

<li><a href="src/README.md"> Código Fonte</a></li>

# Apresentação

<li><a href="presentation/README.md"> Apresentação da solução</a></li>
