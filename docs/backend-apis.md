# APIs e Web Services

O planejamento de uma aplicação de APIS Web é uma etapa fundamental para o sucesso do projeto. Ao planejar adequadamente, você pode evitar muitos problemas e garantir que a sua API seja segura, escalável e eficiente.

Aqui estão algumas etapas importantes que devem ser consideradas no planejamento de uma aplicação de APIS Web.

[Inclua uma breve descrição do projeto.]

## Objetivos da API

O primeiro passo é definir os objetivos da sua API. O que você espera alcançar com ela? Você quer que ela seja usada por clientes externos ou apenas por aplicações internas? Quais são os recursos que a API deve fornecer?

[Inclua os objetivos da sua api.]


## Arquitetura

[Descrição da arquitetura das APIs, incluindo os componentes e suas interações.]

## Modelagem da Aplicação
[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]


## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Requisitos Funcionais

[Liste os principais requisitos funcionais da aplicação.]





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

[Liste os principais requisitos não funcionais da aplicação, como desempenho, segurança, escalabilidade, etc.]

## Tecnologias Utilizadas

Existem muitas tecnologias diferentes que podem ser usadas para desenvolver APIs Web. A tecnologia certa para o seu projeto dependerá dos seus objetivos, dos seus clientes e dos recursos que a API deve fornecer.

[Lista das tecnologias principais que serão utilizadas no projeto.]

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
