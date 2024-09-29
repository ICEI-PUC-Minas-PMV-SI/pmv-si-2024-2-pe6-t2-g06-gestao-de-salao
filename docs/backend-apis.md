# APIs e Web Services

A aplicação "Gestão de Salão" foi desenvolvida para melhorar a experiência de clientes e donos de salões de beleza, oferecendo uma plataforma digital centralizada que facilita o acesso a serviços de beleza. O sistema visa atender a um público diversificado e proporcionar maior conveniência no processo de agendamento, busca por promoções e interação com os salões. Além disso, o projeto busca otimizar os processos internos dos estabelecimentos, oferecendo ferramentas que facilitam o controle de agendas e o relacionamento com os clientes. Com essa abordagem, o "Gestão de Salão" pretende criar uma solução escalável, integrada e eficiente tanto para usuários quanto para salões.

## Objetivos da API

#### API de Cliente: 
Objetivo: Fornecer funcionalidades que aprimorem a interação dos clientes com os salões. Destinada tanto para usuários finais quanto para integração com outros sistemas de parceiros. 
Recursos Esperados:
- Inclusão de clientes: Possibilitar a inclusão de novos clientes no banco de dados.
- Busca por usuário de clientes: Possibilita localizar o cadastro de clientes no banco de dados.
- Atualização de cadastros: Permite a atualização de informações dos clientes, como endereço, telefone, e-mail, etc.
- Exclusão de clientes: Permitir a exclusão de registros de clientes do sistema.

#### API de Agendamento de agendas: 
Objetivo: Facilitar a marcação de horários com agilidade diretamente pelo aplicativo.
Recursos Esperados: 
- Busca por salões: Permite que usuários localizem salões e mostre os serviços que eles oferecem.
- Realização de agendamento: Possibilita que o usuário realize agendamento de serviços em salões.
- Atualização de agendamento: Permite que o usuário modifique o horário dos seus agendamentos.
- Exclusão de agendamentos: Permite que o usuário cancele um agendamento
- Check-in digital: Permitir que os clientes façam check-in de forma antecipada, agilizando o atendimento no salão.

#### API de Serviços: 
Objetivo: Gerenciar o catálogo de serviços oferecidos pelos salões de beleza e facilitar o acesso dos clientes a esses serviços. Destinada a donos de salão para gestão interna e clientes que utilizam a plataforma para buscar e agendar serviços.
Recursos Esperados: 
- Cadastro de serviços: Permitir que os salões adicionem e atualizem os serviços oferecidos, incluindo preços e tempo estimado de execução.
- Consulta de serviços: Disponibilizar aos clientes uma lista detalhada de serviços oferecidos por cada salão, com filtros por tipo de serviço (corte de cabelo, manicure, tratamentos estéticos, etc.).
- Atualização de portfólio: Permitir que os salões modifiquem o portfólio de serviços, incluindo novas opções ou ajustando as existentes.
- Exclusão de serviços: Permitir que os donos de salão removam serviços que não são mais oferecidos.

#### API de Carrinho: 
Objetivo: Gerenciar o carrinho de compras dos usuários, permitindo a seleção e gerenciamento de serviços antes da finalização do agendamento. Destinada a clientes que utilizam a plataforma para escolher serviços e realizar agendamentos. 
Recursos Esperados:
- Adicionar serviço ao carrinho: Permitir que os clientes adicionem serviços ao carrinho enquanto navegam pelo catálogo. Cada serviço selecionado será incluído com detalhes como nome, preço e duração.
- Atualizar itens do carrinho: Oferecer aos clientes a capacidade de modificar os serviços selecionados, como alterar a quantidade (para produtos, se aplicável) ou mudar a data/horário do serviço.
- Remover serviço do carrinho: Permitir a exclusão de um serviço do carrinho de compras, ajustando o total conforme necessário.
- Visualizar carrinho: Disponibilizar uma visão geral do carrinho, incluindo a lista de serviços selecionados, preços totais e possíveis promoções aplicáveis.
- Limpar carrinho: Prover uma opção para que o cliente possa esvaziar completamente o carrinho, removendo todos os itens selecionados de uma vez.

## Arquitetura

[Descrição da arquitetura das APIs, incluindo os componentes e suas interações.]

## Modelagem da Aplicação
[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]


## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Requisitos Funcionais

| ID     | Descrição do Requisito                                                                                         | Tipo                 | Prioridade | Responsável |
|--------|---------------------------------------------------------------------------------------------------------------|----------------------|------------|------------|
| RF-001 | O sistema deve permitir gestão de usuário.                                                                     | USUÁRIO     | ALTA       |Everton De Souza   [github-repo-link](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t2-g06-gestao-de-salao-servico-usuario) <br>    |
| RF-002 | O sistema deve permitir gestão de agenda.                                                                      | AGENDA      | ALTA       |Sara Vidal   [github-repo-agendamentos](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t2-g06-gestao-de-salao-servico-agenda) <br> and  [github-repo-api-gateway](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t2-g06-gestao-de-salao-api-gateway) <br>    |
| RF-003 | O sitema deve permitir gestão de serviços, tais como: serviços oferecidos, qr code service, baixa no sistema, histórico, reviews e etc.       | SERVIÇOS    | BAIXA  |Roberto Santos   [github-repo-link](https://github.com/b3tones/pmv-si-2024-2-pe6-t2-g06-gestao-de-salao-servico-servico.git)    |
| RF-004 | O sistema deve possuir gestão de carrinho                                                                       | PAGAMENTO  | ALTA      |Lucas Nascimento e Sarah Moura  [github-repo-link](https://github.com/Lucasmnclima/mf-Carrinho-compras.git)      |
| RF-005 | O sistema deve possuir sistema de notificação                                                                   | MENSAGEM   | BAIXA     |Patrick Magalhães      |



## Objetivos

Objetivo geral: desenvolvimento de uma aplicação distribuída para gestão de Salão.
Delimitação: iremos nos focar apenas em serviços de beleza.

O objetivo da criação da aplicação é a ideia de maximizar o contato entre clientes e salões. Com a ideia, pretendemos implementar um modo onde cada usuário final possa escolher o melhor serviço e local, com uma pesquisa mais simples e limpa. Ofereceremos praticidade, segurança, conforto, otimização, flexibilidade e modernidade, tanto aos salões, quanto aos clientes.


## Justificativa

Faremos uma aplicação que possa ser estudada e reaproveitada futuramente. A ideia é treinarmos fundamentos de sistema distribuído, integrando o desenvolvimento web e o mobile.

|ID    | Descrição do Requisito  | Tipo |  Prioridade |
|------|-------------------------|----------------|----|
|RF-001| O sistema deve exibir uma tela para login/cadastro/(talvez: Recuperar senha? Caso implementemos, criar os RFs para recuperar senha e modificar o flowchart...) | TELA DE LOGIN - Seleção do Tipo de Usuário | ALTA |
|RF-002| O sistema deve exibir uma opção para o usuário selecionar o que deseja fazer: login ou cadastro | TELA DE LOGIN - Seleção do Login | ALTA |
|RF-003| O sistema deve permitir que o usuário final se auto cadastre com dados como: Email, senha, telefone, CPF. | TELA DE LOGIN - Cadastro de Usuário | ALTA |
|RF-004| O sistema deve permitir que o usuário final e/ou funcionário entrem com o seu CPF, senha e um checkbox "Sou Funcionário?". | TELA DE LOGIN - Entrada de Credenciais existentes | ALTA |
|RF-005| O sistema deve exibir um botão para visualizar/ocultar a senha digitada tanto na tela de login como na tela de cadastro. | TELA DE LOGIN - Entrada de Credenciais existentes | ALTA |
|RF-006| O cadastro de um novo funcionário/profissional só pode ser realizado após o login de um funcionário autorizado da empresa. Usuário padrão = Admin (criado na hora da implementação do sistema no salão). | APÓS LOGIN - Login de Admin | ALTA |
|RF-007| O sistema deve exigir que o Amd autorizado insira os seguintes dados ao cadastrar um novo funcionário/profissional: nome completo do funcionário, e-mail corporativo do funcionário, CPF, telefone, cargo ou especialidade, e CNPJ da empresa. | Cadastro de Colaborador - Cadastro de Novo Funcionário Após Login de Funcionário Autorizado | ALTA |
|RF-008| O sistema deve permitir que o usuário (qualquer tipo) configure seu perfil com mais dados, ou troque sua senha. | TELA DE LOGIN - Cadastro de Novo Funcionário Após Login de Funcionário Autorizado | ALTA |
|RF-009| O sistema deve permitir que o Adm crie, edite e exclua compromissos na agenda geral. | APÓS LOGIN - Gestão de Agendas | ALTA |
|RF-010| O sistema deve permitir que o funcionário/profissional crie, edite e exclua compromissos em sua agenda pessoal. | APÓS LOGIN - Gestão de Agendas para funcionário | ALTA |
|RF-011| O sistema deve permitir que o funcionário/profissional defina a disponibilidade em sua agenda, indicando horários livres e ocupados. | APÓS LOGIN - Gestão de Agendas para funcionário | ALTA |
|RF-012| O sistema deve garantir que apenas o funcionário/profissional autenticado tenha acesso à sua agenda específica, sem visibilidade das agendas de outros profissionais, exceto pela empresa administradora. | APÓS LOGIN - Gestão de Agendas para funcionário | ALTA |
|RF-013| O sistema deve permitir que o funcionário/profissional visualize e gerencie reservas feitas por usuários finais diretamente em sua agenda | APÓS LOGIN - Gestão de Agendas para funcionário | ALTA |
|RF-014| O sistema deve assegurar que cada funcionário/profissional só possa visualizar e editar a sua própria agenda, sem acesso às agendas de outros profissionais ou à agenda corporativa. | APÓS LOGIN - Controle de Acesso à Agenda para funcionário | ALTA |
|RF-015| O sistema deve enviar notificações por e-mail ou WhatsApp para o funcionário/profissional quando um novo compromisso é agendado ou cancelado por um usuário final. | APÓS LOGIN - Notificações para funcionário | BAIXA |
|RF-016| O sistema deve garantir que o acesso a funcionalidades específicas da aplicação seja concedido com base no tipo de usuário (Usuário Final, Empresa ou Funcionário/Profissional). O sistema deve redirecionar o funcionário/profissional para a tela da agenda pessoal após o login.| APÓS LOGIN - Controle de Acesso | ALTA |
|RF-017| O sistema deve redirecionar o usuário final para a tela inicial apropriada após o login (ex.: LISTA DE SALÕES NO RAIO DE 20 KM). | APÓS LOGIN - Redirecionamento Pós-Login | ALTA |
|RF-018| O sistema deve redirecionar a empresa para a tela inicial corporativa após o login (ex.: painel administrativo da empresa). | APÓS LOGIN - Redirecionamento Pós-Login | ALTA |
|RF-019| O sistema deve fornecer uma opção visível para logout em todas as telas pós-login. O sistema deve garantir que o logout encerre completamente a sessão do usuário, exigindo novo login para acessar a aplicação novamente. | LOGOUT | ALTA |
|RF-020| O sistema deve exibir mensagens claras e específicas para erros de login, como "Senha incorreta" ou "E-mail não registrado". | LOGIN - Feedback de Erro | ALTA |
|RF-021| O sistema deve alertar o usuário em caso de tentativa de acesso com uma conta incorreta para o tipo de usuário selecionado. | LOGIN - Feedback de Erro | ALTA |
|RF-022| O sistema deve bloquear a conta após um número específico de tentativas de login falhas e fornecer instruções para desbloqueio. | APÓS LOGIN - Controle de Acesso | BAIXA |
|RF-023| O sistema deve solicitar permissão para acessar a localização atual do usuário ao abrir a tela, ao abrir o app. | ESCOLHA DO SALÃO - Geolocalização | MEDIA |
|RF-024| O sistema deve obter as coordenadas GPS do usuário e utilizá-las para calcular a distância até os salões de beleza próximos. | ESCOLHA DO SALÃO - Geolocalização | MEDIA |
|RF-025| O sistema deve permitir que o usuário insira manualmente um endereço ou CEP, caso não deseje utilizar a localização atual. | ESCOLHA DO SALÃO - Geolocalização | MEDIA |
|RF-026| O sistema deve exibir uma lista de salões de beleza dentro de um raio de 20 quilômetros da localização do usuário. | ESCOLHA DO SALÃO - Listagem de Salões de Beleza | MEDIA |
|RF-027| O sistema deve exibir o nome, endereço, e a distância de cada salão de beleza em relação à localização atual do usuário. | ESCOLHA DO SALÃO - Listagem de Salões de Beleza | MEDIA |
|RF-028| O sistema deve exibir uma imagem representativa do salão de beleza, como uma foto da fachada/interior/logo. | ESCOLHA DO SALÃO - Listagem de Salões de Beleza | MEDIA |
|RF-029| O sistema deve permitir que o usuário visualize a lista de salões em ordem crescente de distância. | ESCOLHA DO SALÃO - Listagem de Salões de Beleza | MEDIA |
|RF-030| O sistema deve permitir que o usuário aplique filtros para refinar a lista de salões de beleza com base em critérios como: Serviços oferecidos (ex.: corte, manicure, coloração), Faixa de preço (ex.: econômico, intermediário, premium), Classificação (ex.: salões com avaliação mínima de 4 estrelas), Disponibilidade de horários | ESCOLHA DO SALÃO - Filtros de Pesquisa | ALTA |
|RF-031| O sistema deve permitir que o usuário clique em um salão de beleza na lista para ver uma página de detalhes. | ESCOLHA DO SALÃO - Detalhes do Salão | ALTA |
|RF-032| O sistema deve exibir uma lista de serviços disponíveis no salão de beleza escolhido. | ESCOLHA DO SERVIÇO - Exibição de Serviços do Salão de Beleza | ALTA |
|RF-033| O sistema deve mostrar para cada serviço: nome, descrição breve, preço e duração estimada. | ESCOLHA DO SERVIÇO - Detalhes do Serviços | ALTA |
|RF-034| O sistema deve permitir que o usuário selecione um ou mais serviços para obter mais detalhes ou adicionar ao carrinho. | ESCOLHA DO SERVIÇO - Detalhes do Serviços | ALTA |
|RF-035| O sistema deve categorizar os serviços por tipos (ex.: Cabelo, Unhas, Maquiagem, etc.) | ESCOLHA DO SERVIÇO - Detalhes do Serviços | ALTA |
|RF-036| O sistema deve permitir que o usuário clique em qualquer serviço para visualizar detalhes adicionais, incluindo fotos, avaliações e profissionais disponíveis. | ESCOLHA DO SERVIÇO - Detalhes e Seleção de Serviços | ALTA |
|RF-037| O sistema deve permitir que o usuário escolha um profissional específico para cada serviço, exibindo uma lista de profissionais disponíveis com base em: Nome do profissional,	Foto do profissional,	Experiência e especializações,	Avaliações e comentários de outros clientes | ESCOLHA DO SERVIÇO - Detalhes e Seleção de Serviços | ALTA |
|RF-038| O sistema deve permitir que o usuário selecione o serviço desejado e adicione-o ao carrinho de compras somente após escolher e passar por todas as etapas de escolha (salao/serviço/profissional/data/hora). | ESCOLHA DO SERVIÇO - Detalhes e Seleção de Serviços | ALTA |
|RF-039| O sistema deve exibir a disponibilidade de horários para cada profissional selecionado antes de adicionar o serviço ao carrinho. | ESCOLHA DO SERVIÇO - Detalhes e Seleção de Serviços | ALTA |
|RF-040| O sistema deve exibir/ter opção para visualizar o carrinho de compras com todos os serviços adicionados, mostrando um resumo que inclui: Nome do serviço,	Nome do profissional selecionado,	Preço de cada serviço, Duração total estimada dos serviços | CARRINHO - Ordem de serviços | ALTA |
|RF-041| O sistema deve permitir que o usuário edite o carrinho, com opção para remover serviços. | CARRINHO - Ordem de serviços | ALTA |
|RF-042| O sistema deve exibir o total a pagar no carrinho, incluindo possíveis taxas ou descontos aplicados. | CARRINHO - Ordem de serviços | ALTA |
|RF-043| O sistema deve permitir que o usuário prossiga para a confirmação do agendamento após revisar os serviços no carrinho. | AGENDA - Agendamento de Serviços | ALTA |
|RF-044| O sistema deve permitir que o usuário confirme o agendamento e visualize um resumo da reserva antes de finalizar. | AGENDA - Agendamento de Serviços | ALTA |
|RF-045| O sistema deve gerar automaticamente um QR code único após a confirmação do agendamento. | AGENDA - Geração de QR Code | ALTA |
|RF-046| O QR code deve conter informações básicas sobre o agendamento, como nome do usuário, data, hora, serviços agendados e os profissionais escolhidos. O sistema deve garantir que o QR code gerado seja único e seguro, evitando duplicações ou fraudes. | AGENDA - Geração de QR Code | ALTA |
|RF-047| O sistema deve exibir o QR code na tela de agendamentos do usuário tal como salvar o agendamento na agenda do salão e funcionário. O sistema deve permitir que o usuário acesse o QR code a qualquer momento a partir da seção de agendamentos. | AGENDA - Geração de QR Code | ALTA |
|RF-048| O sistema deve enviar notificação de novo agendamento para usuário, salao e funcionário (whatsapp ou email). | AGENDA - Geração de QR Code | ALTA |
|RF-049| O sistema deve permitir que o salão de beleza utilize uma máquina ou celular com leitor de QR code para escanear o QR code do usuário na chegada. | AGENDA - Confirmação de Presença e Baixa do Serviço | ALTA |
|RF-050| O sistema deve reconhecer o QR code gerado anteriormente e verificar a validade do agendamento. | AGENDA - Confirmação de Presença e Baixa do Serviço | ALTA |
|RF-051| Após a leitura do QR code, o sistema deve registrar automaticamente a presença do usuário e atualizar o status do serviço como “realizado” no sistema do salão | AGENDA - Confirmação de Presença e Baixa do Serviço | ALTA |
|RF-052| O sistema deve notificar o usuário e o salão de beleza, confirmando que a presença foi registrada e o serviço baixado. | AGENDA - Confirmação de Presença e Baixa do Serviço | ALTA |
|RF-053| O sistema deve solicitar ao usuário uma avaliação do serviço após a confirmação da presença ou conclusão do atendimento. O sistema deve permitir que o usuário deixe um comentário e atribua uma classificação para o serviço e para o profissional que o atendeu. | FEEDBACK - Feedback e Avaliações | BAIXA |

https://miro.com/welcomeonboard/QlVxYUtWaVJ0YVRmZ2NZTHQwYUtBM2k1blBYeU5RR0Q2ZU03ZjhqV2trWHZrZTRJU0NoZjl1dTliTUN6VE9SdnwzNDU4NzY0NTk3Mzc1MTY3ODc0fDI=?share_link_id=369291618323







## Requisitos Não Funcionais

| *ID*      | *Categoria*      | *Descrição*                                                                                                                                                                      | *Prioridade* |
|-----------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RNF-01    | *Desempenho*     | *Tempo de Resposta*: A aplicação deve carregar as principais funcionalidades, como login e seleção de serviços, em até 1 segundo, idealmente medido em milissegundos.             | Alta         |
| RNF-02    | *Desempenho*     | *Escalabilidade*: O sistema deve suportar entre 20 a 100 acessos simultâneos sem perda significativa de desempenho.                                                              | Média        |
| RNF-03    | *Desempenho*     | *Capacidade de Processamento*: A aplicação deve processar múltiplas requisições simultâneas, especialmente durante horários de pico, sem afetar a performance.       | Alta         |
| RNF-04    | *Usabilidade*    | *Interface Amigável*: A interface deve ser intuitiva e otimizada para dispositivos móveis e navegadores web, facilitando a navegação entre páginas de cadastro, escolha de serviços e agendamento. | Alta         |
| RNF-05    | *Usabilidade*    | *Compatibilidade*: A aplicação deve ser responsiva e garantir uma excelente experiência em dispositivos móveis (Android e iOS) e em navegadores web modernos. | Alta         |
| RNF-06    | *Usabilidade*    | *Documentação Básica*: Incluir uma breve documentação ou tutorial que ajude os usuários a entender como usar a aplicação.                                                         | Média        |
| RNF-07    | *Segurança*      | *Autenticação*: Implementar autenticação básica para garantir que apenas pessoas autorizadas possam acessar ou modificar informações.                                                | Alta         |
| RNF-08    | *Segurança*      | *Hashing Simples*: Implementar hashing para senhas utilizando um algoritmo de pelo menos 256 bits para garantir a segurança.                                                     | Alta         |
| RNF-09    | *Segurança*      | *Proteção de Dados Pessoais*: Armazenar dados pessoais dos usuários de forma segura, utilizando o hashing de senhas especificado acima.                                           | Alta         |
| RNF-10    | *Confiabilidade* | *Backup Semanal*: Realizar backups semanais dos dados críticos, com automatização para garantir a segurança e recuperação dos dados.               | Média        |
| RNF-11    | *Confiabilidade* | *Estabilidade Básica*: A aplicação deve funcionar de forma estável durante as demonstrações e testes, sem quedas frequentes.                                                     | Alta         |
| RNF-12    | *Maneabilidade*  | *Código Limpo e Bem Comentado*: Garantir um código organizado e comentado facilita a manutenção e a compreensão por outros desenvolvedores. | Baixa        |
| RNF-13    | *Portabilidade*  | *Compatibilidade com Sistemas Operacionais e Navegadores*: A aplicação deve ser compatível com dispositivos móveis rodando Android e iOS e com navegadores web modernos.   

## Tecnologias Utilizadas

A ideia é desenvolver uma api REST utilizando a linguagem C#(contudo poderá haver uma alteraçao conforme a necessidade e demanda dos integrantes do grupo) e o framework Asp.net core. Para armazenamento foi utilizado o banco de dados relacional MySql. Lista das tecnologias:

| Tecnologia | Aplicação |
|---|---|
| C# | Implementação do Backend |
| Asp.net core | Framework |
| MySql | Banco de Dados |
| Não definido ainda | Deploy da web api |


## API Endpoints

[Liste os principais endpoints da API, incluindo as operações disponíveis, os parâmetros esperados e as respostas retornadas.]

### Endpoint 1
- Método: GET
- URL: /endpoint1
- Parâmetros:
  - param1: [descrição]
- Resposta:
  - Sucesso (200 OK)
    ```
    {
      "message": "Success",
      "data": {
        ...
      }
    }
    ```
  - Erro (4XX, 5XX)
    ```
    {
      "message": "Error",
      "error": {
        ...
      }
    }
    ```


## Considerações de Segurança

Para garantir os requisitos de confidenciabilidade e integridade da api, foi utilizado o JWT, que é um token criptografado de autenticação, com declarações sobre um usuário e uma chave, além dos recursos de autorização do framework asp.net core para restringir o acesso a determinadas funcionalidades da api e recursos anti-fraude.

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

.https://medium.com/beelabacademy/domain-driven-design-vs-arquitetura-em-camadas-d01455698ec5
.https://medium.com/beelabacademy/implementando-na-pr%C3%A1tica-rest-api-com-conceitos-de-ddd-net-core-sql-no-docker-ioc-2cb3a2e7c649
.https://medium.com/beelabacademy/implementando-na-pr%C3%A1tica-rest-api-com-conceitos-de-ddd-net-2160291a44b7
.https://github.com/KleberSouza/mf-apis-web-services-fuel-manager/tree/master
