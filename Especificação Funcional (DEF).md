
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


Sistema detecta uma atualização relevante.

Sistema envia notificação push para o usuário.

Usuário recebe a notificação no dispositivo.

Usuário pode abrir o aplicativo para visualizar detalhes.

8.6 Cenário – Acessar histórico de reservas

Ator: Usuário

Fluxo principal:

Usuário abre o aplicativo.

Usuário realiza login.

Usuário seleciona “Histórico de reservas”.

Sistema consulta as reservas registradas.

Sistema exibe lista de reservas realizadas.

8.7 Cenário – Pagar online

Ator: Usuário

Fluxo principal:

Usuário acessa o sistema.

Usuário realiza login.

Usuário acessa uma reserva realizada.

Sistema apresenta as formas de pagamento disponíveis.

Usuário seleciona o método de pagamento.

Sistema processa o pagamento.

Sistema confirma o pagamento.

Fluxos alternativos:

Pagamento recusado

Sistema informa erro.

Usuário deve escolher outro método ou tentar novamente.

8.8 Cenário – Visualizar informações institucionais

Ator: Usuário

Fluxo principal:

Usuário abre o aplicativo.

Usuário seleciona a opção “Sobre nós”.

Sistema exibe informações sobre:

História do resort

Estrutura

Serviços oferecidos

Usuário visualiza as informações.

8.9 Cenário – Chat com suporte

Ator: Usuário

Fluxo principal:

Usuário abre o aplicativo.

Usuário seleciona o ícone de chat.

Sistema abre a interface de chat.

Usuário envia mensagem ao suporte.

Sistema encaminha a mensagem.

Suporte responde ao usuário.

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