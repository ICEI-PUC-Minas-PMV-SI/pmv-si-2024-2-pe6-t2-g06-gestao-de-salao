# Front-end Web

Este projeto é uma aplicação web destinada a salões de beleza, focada em otimizar o gerenciamento de agendas e serviços. O objetivo principal é facilitar o acesso de salões e clientes a funcionalidades essenciais de agendamento e controle de serviços.

Os salões de beleza podem usar a plataforma para visualizar a agenda de clientes e atualizar o status dos serviços realizados, garantindo um controle eficiente e simplificado das atividades diárias. Já os clientes, ao criar uma conta na aplicação, têm a facilidade de marcar e desmarcar seus agendamentos, gerenciando suas visitas de forma prática e rápida.

Esse projeto visa melhorar a comunicação e a organização entre salões e clientes, proporcionando uma experiência de usuário intuitiva e funcional para ambas as partes.

## Tecnologias Utilizadas
.NET Core: Utilizado no desenvolvimento da API, construído no Visual Studio, garantindo uma base robusta para o backend e facilitando a integração com o front-end e banco de dados.
Arquitetura de Microserviços: A aplicação é organizada em microserviços, promovendo escalabilidade, fácil manutenção e melhor distribuição das responsabilidades entre diferentes serviços.
API Gateway: Implementado para gerenciar e direcionar as requisições aos microserviços corretos, melhorando a segurança e a organização das rotas da aplicação.
React com TypeScript: Utilizado no desenvolvimento do front-end, fornecendo uma interface dinâmica e responsiva para os usuários, com os benefícios da tipagem estática para maior segurança e manutenção do código.
Microsoft SQL Server: Banco de dados centralizado, onde são armazenadas todas as informações essenciais, incluindo os dados dos clientes e agendamentos, permitindo consultas eficientes e seguras.
Essas tecnologias trabalham juntas para fornecer uma aplicação web escalável, organizada e de fácil manutenção, atendendo às necessidades específicas de salões de beleza e de seus clientes.

## Arquitetura

A aplicação adota uma arquitetura de microserviços para facilitar a escalabilidade, modularidade e manutenção. Abaixo, os principais componentes e suas interações:

API Gateway: O ponto de entrada centralizado da aplicação. Todas as requisições dos usuários são direcionadas ao API Gateway, que distribui as chamadas para os microserviços específicos. Ele também fornece segurança, gerenciamento de autorização/autenticação e balanceamento de carga.

Serviço de Autenticação e Autorização: Responsável por gerenciar as credenciais dos usuários e os tokens de autenticação. Utiliza JWT (JSON Web Tokens) para autenticar clientes e salões de beleza, garantindo acesso seguro às funcionalidades da aplicação.

Microserviço de Agendamento: Este serviço lida com o gerenciamento dos agendamentos. Permite que salões de beleza visualizem a lista de clientes agendados e que clientes possam criar, modificar ou cancelar agendamentos.

Microserviço de Cliente: Gerencia os dados dos clientes, como criação de conta, informações pessoais e histórico de agendamentos. Este serviço permite que os clientes mantenham seus dados atualizados e que os salões acessem informações pertinentes aos agendamentos.

Microserviço de Salão: Contém as funcionalidades específicas para o gerenciamento de perfis dos salões de beleza, incluindo informações de serviço e configuração de disponibilidade para agendamentos.

Banco de Dados Centralizado (Microsoft SQL Server): Um banco de dados centralizado onde todas as informações dos clientes, salões e agendamentos são armazenadas. Utilizamos tabelas relacionais e otimizações de consultas para garantir acesso eficiente e seguro aos dados.

Front-End (React com TypeScript): Uma aplicação cliente construída com React e TypeScript, onde clientes e salões interagem diretamente com a interface gráfica. Ele consome as APIs expostas pelos microserviços através do API Gateway.

Fluxo de Interação
Usuário Final: Um cliente ou salão faz login na aplicação através da interface do front-end.
API Gateway: A requisição é encaminhada ao serviço de autenticação para validação.
Microserviços: Uma vez autenticado, o usuário interage com os microserviços de acordo com sua função. Um cliente, por exemplo, pode fazer uma requisição ao microserviço de agendamento para marcar um horário, enquanto um salão pode acessar os detalhes de clientes marcados.
Banco de Dados: Todas as operações são registradas no banco de dados centralizado para persistência e histórico.
Essa arquitetura permite uma aplicação robusta e escalável, onde cada componente é isolado e especializado, promovendo uma estrutura organizada e de fácil manutenção.

## Modelagem da Aplicação
[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]


A modelagem da aplicação foi estruturada com o objetivo de organizar os dados e refletir as principais entidades envolvidas no processo de agendamentos e gerenciamento de salões de beleza. Abaixo, os detalhes da estrutura de dados e as entidades principais:

Estrutura de Dados e Entidades Principais
Usuário:

Representa tanto clientes quanto funcionários do salão (administradores).
Atributos: Id, Nome, Email, Senha, TipoUsuario (cliente ou salão), Telefone, DataCriacao.
Relações: Um usuário (cliente) pode ter vários agendamentos; um usuário (administrador) está relacionado a um ou mais salões.
Salão:

Armazena informações sobre o salão de beleza.
Atributos: Id, Nome, Endereco, Telefone, HorarioFuncionamento, Descricao, IdAdministrador.
Relações: Um salão possui um administrador (usuário do tipo salão) e está vinculado a vários agendamentos.
Agendamento:

Representa os agendamentos entre clientes e salões.
Atributos: Id, DataHora, Status (pendente, confirmado, cancelado), ClienteId, SalaoId, ServicoId.
Relações: Um agendamento está vinculado a um cliente (usuário), a um salão e a um serviço específico.
Serviço:

Contém os tipos de serviços oferecidos pelo salão (ex.: corte de cabelo, manicure).
Atributos: Id, Nome, Descricao, Preco, Duracao.
Relações: Um serviço pode ser oferecido em vários salões e fazer parte de vários agendamentos.
Histórico de Agendamentos:

Armazena o histórico de agendamentos realizados para auditoria e consultas futuras.
Atributos: Id, AgendamentoId, DataAlteracao, StatusAnterior, StatusAtual.
Relações: Está associado a um agendamento específico e contém as mudanças de status ao longo do tempo.
Diagrama de Classes
Abaixo, um exemplo das classes e suas relações:

Usuário

|- Id: int
|- Nome: string
|- Email: string
|- Senha: string
|- TipoUsuario: enum
|- Telefone: string
|- DataCriacao: DateTime
Salão

|- Id: int
|- Nome: string
|- Endereco: string
|- Telefone: string
|- HorarioFuncionamento: string
|- Descricao: string
|- IdAdministrador: int
Agendamento

|- Id: int
|- DataHora: DateTime
|- Status: enum
|- ClienteId: int
|- SalaoId: int
|- ServicoId: int
Serviço

|- Id: int
|- Nome: string
|- Descricao: string
|- Preco: decimal
|- Duracao: int
Histórico de Agendamentos

|- Id: int
|- AgendamentoId: int
|- DataAlteracao: DateTime
|- StatusAnterior: enum
|- StatusAtual: enum
Diagrama de Entidade-Relacionamento (ER)
Usuário (1) -- (n) Agendamento
Salão (1) -- (n) Agendamento
Agendamento (n) -- (1) Serviço
Agendamento (1) -- (n) Histórico de Agendamentos
Considerações
Essa estrutura permite o acompanhamento eficiente de agendamentos e o histórico dos serviços prestados, otimizando o fluxo de trabalho e as consultas de dados, garantindo que a aplicação seja escalável e de fácil manutençã

## Projeto da Interface Web
[Descreva o projeto da interface Web da aplicação, incluindo o design visual, layout das páginas, interações do usuário e outros aspectos relevantes.]

A interface foi projetada para ser intuitiva e eficiente, com design responsivo e paleta de cores neutras. O layout é dividido em:

Página Inicial: Apresentação do salão, serviços e botões de Login/Cadastro.
Cadastro/Login: Formulário para criação de conta e login de clientes e administradores.
Painel do Cliente: Agendamentos futuros, opções de marcação/cancelamento, histórico e perfil.
Painel do Administrador: Visualização da agenda, gerenciamento de clientes e relatórios.
Agendamento: Escolha de serviço, data e hora.
Confirmação e Feedback: Confirmação de agendamentos e formulário de feedback.
A interface é responsiva e acessível, garantindo uma experiência fluida em todos os dispositivos.

### Wireframes
[Inclua os wireframes das páginas principais da interface, mostrando a disposição dos elementos na página.]

### Design Visual
[Descreva o estilo visual da interface, incluindo paleta de cores, tipografia, ícones e outros elementos gráficos.]

### Layout Responsivo
[Discuta como a interface será adaptada para diferentes tamanhos de tela e dispositivos.]

A interface é projetada para se adaptar automaticamente a diversos tamanhos de tela, garantindo acessibilidade e boa usabilidade em dispositivos móveis, tablets e desktops. Os principais pontos incluem:

Componentes Flexíveis: O layout usa um sistema de grids e elementos flexíveis, redimensionando e realocando conteúdo conforme o tamanho da tela.

Navegação Simplificada: Em telas menores, menus laterais se transformam em um menu de ícones ou botões expansíveis, economizando espaço e mantendo as principais funções acessíveis.

Imagens e Botões Redimensionáveis: As imagens, botões e fontes são dimensionados proporcionalmente, proporcionando uma boa experiência de leitura e interação em telas de diferentes resoluções.

Otimização de Conteúdo: Componentes não essenciais são ocultados em dispositivos menores para reduzir o excesso de informações e priorizar funções principais, como agendamento e confirmação de serviços.

Testes de Acessibilidade: Garantimos que o design é adaptável a leitores de tela e utiliza cores com bom contraste, facilitando a navegação para todos os usuários.

Esse layout responsivo assegura que a aplicação funcione bem em qualquer dispositivo, aumentando a satisfação do usuário e incentivando o uso contínuo da plataforma.

### Interações do Usuário
[Descreva as interações do usuário na interface, como animações, transições entre páginas e outras interações.]

## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Requisitos Funcionais

[Liste os principais requisitos funcionais da aplicação.]

## Requisitos Não Funcionais

[Liste os principais requisitos não funcionais da aplicação, como desempenho, segurança, escalabilidade, etc.]


## Considerações de Segurança

[Discuta as considerações de segurança relevantes para a aplicação distribuída, como autenticação, autorização, proteção contra ataques, etc.]

## Implantação

[Instruções para implantar a aplicação distribuída em um ambiente de produção.]

1. Defina os requisitos de hardware e software necessários para implantar a aplicação em um ambiente de produção.
2. Escolha uma plataforma de hospedagem adequada, como um provedor de nuvem ou um servidor dedicado.
3. Configure o ambiente de implantação, incluindo a instalação de dependências e configuração de variáveis de ambiente.
4. Faça o deploy da aplicação no ambiente escolhido, seguindo as instruções específicas da plataforma de hospedagem.
5. Realize testes para garantir que a aplicação esteja funcionando corretamente no ambiente de produção.

## Testes

[Descreva a estratégia de teste, incluindo os tipos de teste a serem realizados (unitários, integração, carga, etc.) e as ferramentas a serem utilizadas.]

1. Crie casos de teste para cobrir todos os requisitos funcionais e não funcionais da aplicação.
2. Implemente testes unitários para testar unidades individuais de código, como funções e classes.
3. Realize testes de integração para verificar a interação correta entre os componentes da aplicação.
4. Execute testes de carga para avaliar o desempenho da aplicação sob carga significativa.
5. Utilize ferramentas de teste adequadas, como frameworks de teste e ferramentas de automação de teste, para agilizar o processo de teste.

# Referências

Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho.
