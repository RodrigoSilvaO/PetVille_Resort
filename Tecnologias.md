
## Tecnologias e Padrões

### 1. Interface Gráfica

### 2. Banco de Dados

### 3. Controle de Versão

#### 3.1 Git
- Utilizado para controle de versão do código fonte.

#### 3.2 GitHub
- Utilizado para hospedagem do repositório do projeto e gerenciamento de issues, milestones e documentação.

### 4. Ambiente de Desenvolvimento

- IDE: Android Studio, Visual Studio Code e/ou Eclipse 

### 5. Processo e práticas

- Controle de versão com Git
- Organização de tarefas com Issues e Milestones no GitHub
- Documentação de requisitos e casos de uso no repositório

### 6. Estrutura tecnológica proposta

- Interface (mobile): Android (Java)
- Lógica do sistema / Backend: Java (Spring Boot) ou outro backend compatível
- Banco de dados: 
- Armazenamento de mídia: S3 ou compatível
- CI/CD: GitHub Actions

## Padrão arquitetural: MVC


O sistema será desenvolvido utilizando o padrão de arquitetura MVC (Model–View–Controller). Esse padrão organiza a aplicação em três camadas principais, promovendo separação de responsabilidades e facilitando a manutenção do código.

As três camadas são:

Model (Modelo): responsável pela representação dos dados do sistema e pelas regras de negócio.

View (Visão): responsável pela interface com o usuário.

Controller (Controlador): responsável por intermediar a comunicação entre a interface e os dados do sistema, controlando o fluxo da aplicação.

Essa arquitetura permite maior organização do código, além de facilitar futuras manutenções e expansões do sistema.

Aplicação no sistema PetVille Resort

No sistema, o padrão MVC será aplicado da seguinte forma:
## Padrão arquitetural: MVC

Breve descrição:
- MVC (Model–View–Controller) separa a aplicação em três camadas: Modelo (dados e regras), Visão (UI) e Controlador (fluxo e coordenação)

- Model: classes que representam entidades do domínio (Pet, Tutor, Reserva) e classes responsáveis por acesso a dados e regras de negócio.
- View: Activities, Fragments e layouts XML que exibem informações e capturam interações do usuário.
- Controller: camadas responsáveis por coordenar a lógica entre View e Model — por exemplo ViewModels, Presenters ou Controllers leves.

Fluxo básico (reserva):
- A View coleta dados do usuário e passa ao Controller.
- O Controller valida e chama serviços/repositórios do Model para persistência e comunicação com backend.
- O resultado é retornado ao Controller, que atualiza a View com sucesso ou erro.

## Padrões de Projeto (Factory, DAO, Singleton)

Factory (Fábrica)
- Propósito: centralizar e encapsular a criação de objetos, especialmente quando a construção é complexa ou depende de configuração.
- Uso sugerido: criar instâncias de serviços, gerenciadores de imagens, provedores de configuração ou objetos que variam por ambiente.

DAO (Data Access Object)
- Propósito: separar a lógica de acesso a dados da lógica de negócio, oferecendo uma API clara para operações de persistência.
- Uso sugerido: criar um DAO por entidade principal (Pet, Tutor, Reserva) tanto para persistência local (Room) quanto para camadas de acesso no backend (JPA/Repository).

Singleton
- Propósito: garantir uma única instância de componentes globais durante o ciclo de vida da aplicação (por exemplo clientes HTTP, cache, gerenciador de sessão).
- Uso sugerido: instâncias únicas para cliente de API, gerenciador de sincronização ou cache em memória.

Como os padrões devem funcionar:
- A View chama um Controller/ViewModel para iniciar uma ação.
- O Controller solicita um serviço ao Factory, que devolve a implementação correta do serviço.
- O serviço utiliza DAOs para persistir dados localmente e prepara chamadas ao backend.
- Para comunicação externa, o serviço utiliza um cliente global (Singleton) para enviar/receber informações.
- Em caso de erro de rede, o serviço marca a operação como pendente e aciona um componente de sincronização que tentará reenviar quando houver conectividade.

