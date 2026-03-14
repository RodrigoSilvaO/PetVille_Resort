
# **Documento de Especificação Funcional (DEF)**

---

## 0. Visão geral do projeto

- **Nome do Software**:Aplicativo PetVille Resort
- **Versão:** 2.0
- **Data:** \[19/11/2025\]
- **Autor(es):** \[Diego Vinicius e Rodrigo da Silva\]
- **Aprovado por:** \[Andre Madureira \]

## 1. Introdução

### 1.1 Propósito

Este documento descreve as funcionalidades, interfaces e comportamentos esperados para o Aplicativo PetVille Resort, cujo objetivo é permitir que tutores realizem reservas, acompanhem a estadia e tenham acesso a informações e serviços oferecidos pelo resort para cães e gatos.

### 1.2 Escopo

O aplicativo permitirá aos usuários:

* Cadastrar perfis pessoais e perfis dos pets;
* Realizar reservas de hospedagem;
* Escolher serviços adicionais (banho, tosa, alimentação personalizada, veterinário);
* Acompanhar a estadia do pet por meio de fotos, vídeos e relatórios diários ;
* Receber notificações sobre atividades e cuidados;
* Visualizar informações institucionais e estrutura do resort.

O sistema será desenvolvido para Android e iOS, sendo projetado para uso por tutores de animais domésticos, especialmente cães e gatos.

### 1.3 Definições, acrônimos e abreviações

| Termo   |               Definição                           |
| ------- | ------------------------------------------------- |
| DEF     | Documento de Especificação Funcional              |
| App     | Aplicativo móvel                                  |
| Tutor   | Usuário responsável pelo animal                   |
| Pet     | Cão ou gato hospedado no resort                   |
| LGPD    | Lei Geral de Proteção de Dados                    |


## 2. Descrição Geral

### 2.1 Perspectiva do Produto

O aplicativo será um sistema independente, conectado ao servidor do PetVille Resort para gerenciamento de reservas, envio de mídias e comunicação. Todo o fluxo de uso será mobile-first e voltado à praticidade.

### 2.2 Funções do Produto

O sistema deve oferecer as seguintes funcionalidades:

* Cadastro e autenticação de usuários;
* Cadastro de pets;
* Consulta de disponibilidade e realização de reservas;
* Seleção de tipos de quarto e serviços adicionais;
* Recebimento de atualizações da estadia;
* Notificações em tempo real;
* Chat entre usuário e equipe;
* Acesso ao histórico de reservas;
* Pagamento online.

### 2.3 Características dos Usuários

Os usuários são tutores de pets, possuindo familiaridade básica com smartphones. Não são necessários conhecimentos técnicos adicionais.

### 2.4 Restrições

* O aplicativo deve ser compatível com Android 10+ e iOS 12+.
* O sistema deve operar conforme diretrizes da LGPD.
* O envio de fotos e vídeos deve ocorrer apenas via Wi-Fi ou Internet móvel ativa.
* A aplicação exige conexão com a internet para a maior parte das funcionalidades.

### 2.5 Suposições e Dependências

* O usuário possui conexão estável com internet.
* Os servidores do PetVille Resort permanecem ativos para envio/recebimento de dados.
* O usuário fornecerá informações verídicas sobre o pet.

---

## 3. Requisitos Funcionais (RF)

| Código |                                          Descrição                                                   |
| ------ | ---------------------------------------------------------------------------------------------------- |
| RF001  | O sistema deve permitir o cadastro de usuário com nome, e-mail, telefone e senha.                          |
| RF002  | O sistema deve permitir o cadastro de pets (nome, espécie, raça, idade, peso, necessidades especiais).                                                                                                     |
| RF003  | O usuário deve poder consultar disponibilidade de hospedagem com seleção de datas, tipo de quarto e serviços extras.                                                                                                |
| RF004  | O sistema deve permitir reserva de hospedagem e geração de comprovante digital.                      |
| RF005  | O app deve exibir opções de serviços adicionais: banho, tosa, alimentação personalizada, veterinário.|
| RF006  | O sistema deve permitir pagamento via cartão de crédito, Pix ou boleto.                              |
| RF007  |  O usuário deve receber notificações push sobre atividades do pet (passeios, brincadeiras, alimentação,etc.).                                                                                             |
| RF008  | A equipe deve poder enviar fotos, vídeos e relatórios diários da estadia do pet.                                                                                                            |
| RF009  | O usuário deve poder visualizar um painel com atualizações da estadia (humor, atividades, saúde, alimentação).                                                                                                   |
 | RF010  | O sistema deve permitir um chat direto entre usuário e equipe.                                      |
 | RF011 |  O usuário deve poder acessar histórico completo de reservas e serviços utilizados.                  |
 | RF012 | O app deve conter uma seção com informações institucionais, estrutura física e serviços do resort.   |
 | RF013 | O usuário deve poder avaliar serviços após a estadia do pet.                                         |
 | RF014 | O sistema deve permitir edição e exclusão dos cadastros do usuário e dos pets.                       |
---

## 4. Requisitos Não Funcionais (RNF)

| Código |                               Descrição                                                |
| ------ | -------------------------------------------------------------------------------------- |
| RNF001 |  O tempo de resposta para carregamento de telas deve ser inferior a 3 segundos.        |
| RNF002 | A interface deve seguir princípios de usabilidade e acessibilidade (alto contraste,
textos legíveis).                                                                                 |
| RNF003 | O sistema deve criptografar dados sensíveis, incluindo senhas e informações pessoais.  |
| RNF004 |O app deve estar disponível 99% do tempo.                                               |
| RNF005 |A comunicação deve seguir protocolos seguros (HTTPS).                                   |
| RNF006 |O aplicativo deve ser otimizado para baixo consumo de bateria e dados móveis.           |
| RNF007 | O código deve seguir boas práticas de modularidade e manutenibilidade.                 |
| RNF008 |O app deve estar em conformidade com a LGPD.                                            |
---

## 5. Interfaces do Sistema

### 5.1 Interface do Usuário

A interface deve conter:

* Tela de login e cadastro;
* Tela de cadastro dos pets;
* Tela de disponibilidade e reserva;
* Tela de serviços adicionais;
* Tela de pagamento;
* Painel de acompanhamento da estadia com fotos, vídeos e relatórios;
* Tela de chat com a equipe;
* Tela com informações sobre o resort;
* Tela de avaliações;
* Configurações do usuário.


### 5.2 Interfaces de Hardware

Não se aplicam.

### 5.3 Interfaces de Software

* 
* 

### 5.4 Interfaces de Comunicação

O sistema utilizará comunicação via internet (Wi-Fi/4G/5G) por protocolo HTTPS.


## 6. Requisitos de Qualidade

| Atributo         | Descrição                                                                 |
| ---------------- | ------------------------------------------------------------------------- |
| Usabilidade      | Interface simples, intuitiva e acessível para usuários de todas as idades.|
| Confiabilidade   | Alta disponibilidade e segurança no processamento de dados.               |
| Manutenibilidade | Estrutura modular e documentação clara para facilitar melhorias futuras.  |
| Portabilidade    | Suporte completo a dispositivos Android e iOS.                            |
| Eficiência       | Boa performance no carregamento de dados e envio de mídias.               |

## 7. Casos de Uso

### 7.1. Cadastrar perfil de usuário 

- Usuário abre sistema
- Usuário seleciona "Cadastrar-se"
- Usuário preenche os campos nome, e-mail, telefone e senha
- Usuário pressiona botão "Cadastrar-se"
- Usuário é cadastrado no sistema.

### 7.2. Cadastrar pet

- Usuário abre sistema
- Usuário faz login no sistema com sua conta
- Usuário seleciona "Cadastrar pet"
- Usuário preenche os campos nome, espécie, raça, idade, peso e necessidades especiais.
- Usuário pressiona botão "Cadastrar"
- Usuário tem o pet cadastrado no sistema e associado à sua conta

### 7.3. Consultar disponibilidade

- Usuário abre sistema
- Usuário faz login 
- Usuário seleciona "Verificar disponibilidade" 
- Sistema mostra os dados
- Usuário pode escolher filtros: Data, tipo de quarto e serviço extra

### 7.4. Realizar reservas

- Usuário abre sistema
- Usuário faz login no sistema 
- Usuário seleciona "Fazer reserva"
- Usuário seleciona Tipo de quarto e (se houver) serviços extras
- Usuário define o pet
- Usuário conclui reserva
- Sistema realiza a reserva
- Sistema exibe na ela um comprovate digital de reserva

### 7.5. Notificar atualizações 

- Notificação push implementada
- Sistema notifica usuário sobre atualizações 

### 7.6. Acessar histórico de reservas

- Usuário abre sistema
- Usuário faz login no sistema
- Usuário seleciona "Histórico de reservas"
- Sistema exibe em formato de histórico todas as reservas realizadas

### 7.7. Pagar online

- Usuário abre sistema
- Usuário faz login no sistema
- Usuário, após ter feito a reserva, aparece as formas de pagamento 

### 7.8. Visualizar informações institucionais e estrutura do resort
- Usuário abre sistema
- Usuário seleciona "Sobre nós"
- Sistema abre uma tela com informações do Resort

### 7.9. Chat
- Usuário abre sistema
- Usuário seleciona o botão com ícone de chat
- Sistema abre o chat com conexão Usuário - Suporte

## 8. Cenários de Uso

### 8.1 Cenário – Cadastrar perfil de usuário
**Ator:** Usuário

**Fluxo principal:**
1. Usuário abre o aplicativo.
2. Usuário seleciona a opção “Cadastrar-se”.
3. Sistema exibe formulário de cadastro.
4. Usuário preenche os campos nome, e-mail, telefone e senha.
5. Usuário pressiona o botão “Cadastrar-se”.
6. Sistema valida os dados informados.
7. Sistema registra o usuário no banco de dados.
8. Sistema confirma o cadastro e permite acesso ao sistema.

**Fluxos alternativos:**
- E-mail já cadastrado:
  1. Sistema identifica e-mail existente.
  2. Sistema exibe mensagem de erro.
  3. Usuário deve inserir outro e-mail.
- Campos obrigatórios não preenchidos:
  1. Sistema solicita preenchimento dos campos faltantes.

### 8.2 Cenário – Cadastrar pet
**Ator:** Usuário

**Fluxo principal:**
1. Usuário acessa o aplicativo.
2. Usuário realiza login.
3. Usuário seleciona a opção “Cadastrar pet”.
4. Sistema exibe formulário de cadastro.
5. Usuário preenche nome, espécie, raça, idade, peso e necessidades especiais.
6. Usuário seleciona “Cadastrar”.
7. Sistema registra o pet no banco de dados.
8. Sistema associa o pet à conta do usuário.
9. Sistema confirma o cadastro.

**Fluxos alternativos:**
- Campos obrigatórios não preenchidos:
  1. Sistema solicita preenchimento correto dos campos obrigatórios.

### 8.3 Cenário – Consultar disponibilidade
**Ator:** Usuário

**Fluxo principal:**
1. Usuário abre o sistema.
2. Usuário realiza login.
3. Usuário seleciona “Verificar disponibilidade”.
4. Sistema exibe opções de pesquisa.
5. Usuário define filtros: data, tipo de quarto e serviços extras.
6. Sistema processa a busca.
7. Sistema exibe os quartos disponíveis.

**Fluxos alternativos:**
- Nenhuma disponibilidade encontrada:
  1. Sistema informa que não há vagas para a data selecionada.

### 8.4 Cenário – Realizar reserva
**Ator:** Usuário

**Fluxo principal:**
1. Usuário abre o aplicativo.
2. Usuário faz login.
3. Usuário seleciona "Fazer reserva".
4. Sistema exibe opções de quartos disponíveis.
5. Usuário escolhe tipo de quarto e serviços extras (opcionais).
6. Usuário seleciona o pet que ficará hospedado.
7. Usuário confirma a reserva.
8. Sistema registra a reserva.
9. Sistema gera comprovante digital de reserva.
10. Sistema exibe confirmação na tela.

**Fluxos alternativos:**
- Quarto indisponível:
  1. Sistema informa indisponibilidade.
  2. Usuário deve escolher outra opção.

### 8.5 Cenário – Notificar atualizações
**Ator:** Sistema

**Fluxo principal:**
1. Sistema detecta uma atualização relevante (ex.: foto, relatório, evento de saúde).
2. Sistema envia notificação push para o usuário.
3. Usuário recebe a notificação no dispositivo.
4. Usuário pode abrir o aplicativo para visualizar detalhes.

### 8.6 Cenário – Acessar histórico de reservas
**Ator:** Usuário

**Fluxo principal:**
1. Usuário abre o aplicativo.
2. Usuário realiza login.
3. Usuário seleciona “Histórico de reservas”.
4. Sistema consulta as reservas registradas.
5. Sistema exibe lista de reservas realizadas.

### 8.7 Cenário – Pagar online
**Ator:** Usuário

**Fluxo principal:**

1. Usuário acessa o sistema.
2. Usuário realiza login.
3. Usuário acessa uma reserva realizada.
4. Sistema apresenta as formas de pagamento disponíveis.
5. Usuário seleciona o método de pagamento.
6. Sistema processa o pagamento.
7. Sistema confirma o pagamento.

**Fluxos alternativos:**
- Pagamento recusado
1. Sistema informa erro.
- Usuário deve escolher outro método ou tentar novamente.

### 8.8 Cenário – Visualizar informações institucionais
**Ator: Usuário**

**Fluxo principal:**

1. Usuário abre o aplicativo.
2. Usuário seleciona a opção “Sobre nós”.
3. Sistema exibe informações sobre:
4. História do resort
5. Estrutura
6. Serviços oferecidos
7. Usuário visualiza as informações.

### 8.9 Cenário – Chat com suporte
**Ator: Usuário**

**Fluxo principal:**

1. Usuário abre o aplicativo.
2. Usuário seleciona o ícone de chat.
3. Sistema abre a interface de chat.
4. Usuário envia mensagem ao suporte.
5. Sistema encaminha a mensagem.
6. Suporte responde ao usuário.

## **9. Casos de Teste (CT)**  

| **Caso de Teste**        | **Entrada** | **Resultado Esperado** |
| ------------------------ | ----------- | ---------------------- |
|CT001 (Cadastrar usuário)|Dados usuário|Usuário cadastrado no sistema
|CT002 (Cadastrar pet)|Dados do pet|Pet cadastrado e anexado a conta de usuário
|CT003 (Visualizar informações)|Clique no botão "Sobre nós"|Abrir tela com informações sobre o resort
|CT004 (Consultar disponibilidade)|Clique no botão "Verificar disponibilidade"|Sistema exibe os quartos disponíveis
|CT005 (Realizar reserva)|Dados da reserva (pet, quarto, serviços extras)|Reserva registrada no sistema
|CT006 (Histórico de reservas)|Clique no botão "Histórico de reservas"|Sistema exibe o histórico de reservas do usuário
|CT007 (Pagamento online)|Escolha da forma de pagamento|Sistema processa o pagamento da reserva
|CT008 (Notificação de atualização)|Atualização no sistema|Usuário recebe notificação sobre a atualização
|CT009 (Acessar chat)|Clique no ícone de chat|Sistema abre o chat com suporte