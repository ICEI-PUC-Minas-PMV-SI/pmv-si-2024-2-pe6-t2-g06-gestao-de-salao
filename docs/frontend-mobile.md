# Front-end Móvel

O projeto "Gestão de Salão" tem como objetivo proporcionar uma experiência prática e eficiente para clientes e salões de beleza, facilitando o agendamento de serviços, pagamentos e check-ins digitais por meio de uma aplicação móvel. A aplicação visa atender às necessidades do público-alvo conectado, oferecendo uma interface intuitiva e moderna para dispositivos Android e iOS. Os objetivos principais do projeto são:
- Facilitar a busca por serviços e profissionais com base em diferentes critérios.
- Permitir o agendamento de serviços de maneira rápida e segura.
- Fornecer informações detalhadas sobre os serviços e agendamentos.
- Oferecer uma interface amigável e acessível em diversos dispositivos móveis.



## Tecnologias Utilizadas

- Front-end: React Native
- Gerenciamento de Estado: Redux
- Design: Figma (para prototipagem e wireframes)
- Comunicação com Backend: Axios (consumo de APIs RESTful)
- Estilização: Styled Components
- Testes: Jest e React Native Testing Library

## Arquitetura

Para garantir uma organização robusta, manutenibilidade e escalabilidade na aplicação, adotaremos o padrão de arquitetura MVVM (Model-View-ViewModel). Essa abordagem divide as responsabilidades em camadas bem definidas, promovendo uma separação clara entre interface, lógica de negócios e manipulação de dados.

A seguir, detalharemos como cada camada será implementada:

**View:** Componentes desenvolvidos em React Native, responsáveis por apresentar a interface do usuário e capturar interações.  
**ViewModel**: A camada intermediária que concentra a lógica de negócios, gerencia o estado da aplicação e atua como um elo entre a View e o Model.  
**Model:** Representa os dados do domínio e suas operações, além de encapsular a comunicação com a API para acesso e manipulação das informações.  

Essa arquitetura proporciona uma estrutura modular e escalável, ideal para projetos que demandam evolução constante e manutenção eficiente.

## Modelagem da Aplicação
[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]

## Projeto da Interface

A interface do aplicativo terá foco na simplicidade e clareza. Os principais elementos incluem:

- Página inicial com botões de login e cadastro.
- Dashboard para visualizar agendamentos e status.
- Seção para pesquisa e agendamento de serviços.
- Seção para pagamento.

## Wireframes

Os wireframes principais incluem:

#### Tela de Login:

  <img src = "img/tl1.png">

  <img src = "img/tl2.png">
  

#### Tela de HomePage:

<img src = "img/hp1.png">

  
#### Tela de Agendamento:

<img src = "img/la1.png">

<img src = "img/la2.png">

<img src = "img/pd1.png">

  
#### Tela de Listagem de serviços:

<img src = "img/ls1.png">

<img src = "img/ls2.png">
  

### Design Visual

O design visual da aplicação foi pensado para proporcionar uma experiência de usuário moderna, atraente e intuitiva, alinhada às tendências contemporâneas de interface e experiência de usuário (UI/UX). As decisões visuais foram cuidadosamente planejadas para criar um ambiente harmônico, acessível e funcional, com base nos seguintes aspectos:

- Paleta de cores: Tons de laranja (#FF7043) e cinza claro para destacar elementos principais.
- Tipografia: Fontes modernas como Roboto para legibilidade.
- Ícones: Uso de biblioteca como Material Icons para consistência visual.

### Layout Responsivo

O layout do aplicativo foi projetado para ser totalmente responsivo, garantindo uma experiência consistente e intuitiva em dispositivos com diferentes tamanhos de tela, como smartphones e tablets. O foco está em atender às necessidades do usuário sem comprometer a usabilidade e a estética, independentemente do dispositivo utilizado.

#### Smartphones:
Interface otimizada para telas menores, com foco em navegação simplificada e botões maiores, evitando toques acidentais.
Elementos críticos, como botões de ação, localizados nas áreas de fácil alcance (thumb-friendly zones).

#### Tablets:
Design ajustado para aproveitar o espaço adicional, com layouts em grade (grid-based) que permitem exibir mais informações de forma organizada.
Ajustes em margens e espaçamentos para evitar desperdício de espaço e melhorar a leitura visual.

### Interações do Usuário
[Descreva as interações do usuário na interface, como animações, transições entre páginas e outras interações.]


- Animações: Feedback visual para cliques e transições.
- Transições: Navegação suave entre páginas utilizando a biblioteca React Navigation.
- Gestos: Swipe para exclusão ou edição de agendamentos.

## Fluxo de Dados

<img src = "img/fluxoMiro.png">
O fluxo de dados na aplicação segue uma arquitetura de microserviços, garantindo que cada componente lide de maneira eficiente e independente com suas próprias funções. Abaixo está uma descrição simplificada do fluxo:

Solicitações do Usuário: O cliente (usuário final) acessa a interface web através do navegador, onde pode realizar ações como criar uma conta, agendar um serviço, ou gerenciar seus agendamentos.

Front-end (React TS): A interface web em React TS recebe as interações dos usuários e se comunica com o back-end para enviar ou receber dados via API.

API Gateway: Todas as solicitações do front-end passam pelo API Gateway, que gerencia as rotas e distribui as requisições aos microserviços corretos, garantindo segurança e escalabilidade.

Microserviços: Cada microserviço é responsável por uma função específica, como:

Autenticação: valida as credenciais dos usuários.
Agenda: gerencia agendamentos de serviços.
Clientes: gerencia informações dos clientes e o histórico de serviços.
Banco de Dados (SQL Server): Os dados são armazenados de forma centralizada no Microsoft SQL Server, onde são salvos e recuperados conforme necessário, incluindo informações de usuários, agendamentos, e histórico de serviços.

Resposta ao Cliente: Após o processamento da solicitação, o back-end retorna os dados para o front-end através do API Gateway, onde são exibidos ao usuário na interface.

Esse fluxo permite uma comunicação organizada e eficiente, garantindo que cada ação seja rapidamente processada e retornada ao usuário.

## Requisitos Funcionais

O aplicativo foi projetado para atender às principais necessidades dos usuários e dos estabelecimentos parceiros, integrando funcionalidades que oferecem praticidade, segurança e eficiência. A seguir, são detalhadas os requisitos funcionais mapeados:

| ID     | Descrição do Requisito                                                                                        | Tipo        |  Prioridade|
|--------|---------------------------------------------------------------------------------------------------------------|-------------|------------|
| RF-001 | Permitir que novos usuários se registrem na plataforma de forma simples e rápida.                             | BACKEND     | ALTA       |
| RF-002 | Garantir acesso seguro aos usuários já cadastrados                                                            | BACKEND     | ALTA       |
| RF-003 | Permitir que os usuários explorem os serviços oferecidos pelos salões de beleza parceiros                     | FRONTEND    | ALTA       |
| RF-004 | O sistema deve permitir agendamento de serviços para usuário cadastrados                                      | BACKEND     | ALTA       |

## Requisitos Não Funcionais

O sistema foi projetado para garantir alta eficiência, compatibilidade, segurança e escalabilidade, atendendo às expectativas de qualidade e experiência dos usuários. A seguir, são apresentados os requisitos não funcionais definidos para a aplicação:

| ID     | Descrição do Requisito                                                                                        | Tipo        |  Prioridade|
|--------|---------------------------------------------------------------------------------------------------------------|-------------|------------|
| RF-001 | O sistema deve ser eficiente, oferecendo tempos de resposta ágeis inferiores a 2 segundos.                    | PERFORMANCE | ALTA       |
| RF-002 | Suporte para versões recentes de Android e iOS                                                                | COMPATIBILIDADE | ALTA   |
| RF-003 | Proteger os dados sensíveis dos usuários contra acessos não autorizados                                       | SEGURANÇA   | ALTA       |
| RF-004 | Garantir que o aplicativo seja fácil de manter e possa crescer conforme necessário                            | ESCALABILIDADE| ALTA     |

## Considerações de Segurança

A segurança é um aspecto essencial no desenvolvimento de aplicações, especialmente em sistemas que lidam com dados sensíveis e informações pessoais dos usuários. O aplicativo foi projetado com uma abordagem de "Security by Design", onde práticas e tecnologias de segurança são integradas desde as primeiras fases do desenvolvimento. Abaixo, são detalhadas as principais medidas adotadas para garantir a proteção do sistema, dos dados dos usuários e a conformidade com regulamentações:

#### Autenticação e Controle de Sessão:
- Implementação de autenticação baseada em JSON Web Tokens (JWT), garantindo que apenas usuários autenticados possam acessar recursos protegidos.
- Os tokens incluem tempo de expiração e são assinados com chaves criptográficas robustas para evitar falsificações ou reutilizações.
- Mecanismos de logout ativo e invalidação de tokens comprometidos, aumentando a proteção contra sequestro de sessões.
  
#### Comunicação segura com o backend por meio de HTTPS:
- Todas as comunicações entre o cliente e o servidor utilizam o protocolo HTTPS, que emprega certificados SSL/TLS para garantir criptografia ponta a ponta.
- Reforço da segurança contra ataques de "man-in-the-middle" (MITM) por meio de validação rigorosa de certificados e uso de HSTS (HTTP Strict Transport Security).

## Implantação

[Instruções para implantar a aplicação distribuída em um ambiente de produção.]

1. Defina os requisitos de hardware e software necessários para implantar a aplicação em um ambiente de produção.
2. Escolha uma plataforma de hospedagem adequada, como um provedor de nuvem ou um servidor dedicado.
3. Configure o ambiente de implantação, incluindo a instalação de dependências e configuração de variáveis de ambiente.
4. Faça o deploy da aplicação no ambiente escolhido, seguindo as instruções específicas da plataforma de hospedagem.
5. Realize testes para garantir que a aplicação esteja funcionando corretamente no ambiente de produção.

- Requisitos de Hardware e Software:
- Servidores na AWS para backend e base de dados.
- Serviços como Firebase para notificações.
- Hospedagem: Uso de plataformas como Google Play Store e Apple App Store.
- Deploy: Configuração do ambiente com Expo CLI ou ferramentas nativas (Android Studio/Xcode).
- Testes de Produção: Realizar testes beta com TestFlight (iOS) e Google Play Console (Android).



## Testes

[Descreva a estratégia de teste, incluindo os tipos de teste a serem realizados (unitários, integração, carga, etc.) e as ferramentas a serem utilizadas.]

1. Crie casos de teste para cobrir todos os requisitos funcionais e não funcionais da aplicação.
2. Implemente testes unitários para testar unidades individuais de código, como funções e classes.
3. Realize testes de integração para verificar a interação correta entre os componentes da aplicação.
4. Execute testes de carga para avaliar o desempenho da aplicação sob carga significativa.
5. Utilize ferramentas de teste adequadas, como frameworks de teste e ferramentas de automação de teste, para agilizar o processo de teste.

- Unitários: Validação de componentes individuais.
- Integração: Testes do fluxo de autenticação e agendamento.
- Carga: Simulação de múltiplos usuários.
- Ferramentas: Jest, React Native Testing Library, e Expo CLI para debugging.


# Referências

- Documentação do React Native: https://reactnative.dev/
- Material Design Guidelines: https://material.io/design
