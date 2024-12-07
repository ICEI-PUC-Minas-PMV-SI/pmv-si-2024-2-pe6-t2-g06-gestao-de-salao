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

A arquitetura da aplicação será baseada no padrão MVVM (Model-View-ViewModel):

- View: Componentes React Native que representam a interface do usuário.
- ViewModel: Contém a lógica de negócios e gerencia o estado da aplicação.
- Model: Representa os dados do domínio e interage diretamente com a API.

## Modelagem da Aplicação
[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]

## Projeto da Interface

A interface do aplicativo terá foco na simplicidade e clareza. Os principais elementos incluem:

- Página inicial com botões de login e cadastro.
- Dashboard para visualizar agendamentos e status.
- Seção para pesquisa e agendamento de serviços.
- Seção para pagamento.

### Wireframes
[Inclua os wireframes das páginas principais da interface, mostrando a disposição dos elementos na página.]


Os wireframes principais incluem:

- Tela de Login:
  
- Tela de Cadastro:
  
- Tela de Agendamento:
  
- Tela de Pagamento:
  
- Tela de Listagem de serviços:
  

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

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Requisitos Funcionais
[Liste os principais requisitos funcionais da aplicação.]


- Cadastro de usuários.
- Login e autenticação.
- Visualização de serviços disponíveis.
- Agendamento de serviços.
- Sistema de pagamento.

## Requisitos Não Funcionais
[Liste os principais requisitos não funcionais da aplicação, como desempenho, segurança, escalabilidade, etc.]

- Alta usabilidade e tempos de resposta inferiores a 2 segundos.
- Suporte para versões recentes de Android e iOS.
- Segurança no armazenamento de dados sensíveis.



## Considerações de Segurança
[Discuta as considerações de segurança relevantes para a aplicação distribuída, como autenticação, autorização, proteção contra ataques, etc.]

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
