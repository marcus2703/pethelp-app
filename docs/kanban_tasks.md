# Backlog de tarefas para o quadro Kanban

Este documento detalha as tarefas de desenvolvimento prontas para a equipe, alinhadas com as Histórias de Usuário e formatadas como cards para o Kanban.

---

### **Épico: Engajamento e Relato (Cidadão)**

<br>

**Card 1: API para submissão de relatos**
* **História Relacionada:** HU-CID-001, HU-CID-003
* **Tags:** `BE`, `API`, `DB`
* **Descrição:** Construir e testar o endpoint `POST /api/reports` que recebe os dados de um novo relato (incluindo a imagem), valida as informações e as persiste no banco de dados, retornando uma resposta de sucesso.
* **Checklist de Tarefas:**
    * [ ] Definir a rota e o controller para `POST /api/reports`.
    * [ ] Implementar a validação do corpo da requisição (payload).
    * [ ] Integrar com o serviço de upload de imagens.
    * [ ] Criar o serviço para salvar os dados na tabela `reports`.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A funcionalidade opera conforme o esperado no ambiente de testes.
    * ✅ A documentação da API foi atualizada.

<br>

**Card 2: UI da tela de novo relato**
* **História Relacionada:** HU-CID-003, HU-CID-004
* **Tags:** `FE`, `UI`, `Mobile`
* **Descrição:** Desenvolver o componente da tela "Novo Relato", permitindo que o usuário preencha o formulário, acesse a câmera e o GPS, e envie os dados para a API.
* **Checklist de Tarefas:**
    * [ ] Estruturar o layout da tela com os campos e o botão de envio.
    * [ ] Implementar a integração com a API nativa da Câmera e GPS.
    * [ ] Desenvolver a lógica para gerenciar o estado do formulário.
    * [ ] Criar a função que envia os dados para o endpoint da API.
    * [ ] Implementar o feedback visual para o usuário (loading, sucesso/erro).
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A interface funciona conforme o design de UI/UX.
    * ✅ A funcionalidade foi testada e validada no ambiente de testes.

<br>

**Card 3: API para autenticação e cadastro de usuários**
* **História Relacionada:** HU-CID-002, HU-ONG-001
* **Tags:** `BE`, `API`, `Auth`, `DB`
* **Descrição:** Implementar os endpoints `POST /api/auth/register` e `POST /api/auth/login` para o cadastro e autenticação de usuários (Cidadão e ONG), retornando um token JWT.
* **Checklist de Tarefas:**
    * [ ] Modelar a tabela `users` com campos para perfil (role), status, etc.
    * [ ] Implementar a lógica de hashing de senhas.
    * [ ] Criar o endpoint de registro, validando os dados de entrada.
    * [ ] Criar o endpoint de login, validando as credenciais.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A funcionalidade opera conforme o esperado no ambiente de testes.
    * ✅ A documentação da API foi atualizada.

<br>

**Card 4: UI das telas de login e cadastro**
* **História Relacionada:** HU-CID-002, HU-ONG-001
* **Tags:** `FE`, `UI`, `Auth`
* **Descrição:** Desenvolver as telas de Login, a tela de escolha de perfil ("Cidadão" ou "ONG"), e os respectivos formulários de cadastro, integrando-os com a API de autenticação.
* **Checklist de Tarefas:**
    * [ ] Criar a tela de Login e a tela de Pré-Cadastro.
    * [ ] Desenvolver o formulário de cadastro simples para Cidadão.
    * [ ] Desenvolver o formulário de cadastro detalhado para ONG.
    * [ ] Integrar os formulários com os endpoints da API de autenticação.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A interface funciona conforme o design de UI/UX.
    * ✅ A funcionalidade foi testada e validada no ambiente de testes.

<br>

**Card 5: API para sinalização de relatos**
* **História Relacionada:** HU-CID-005
* **Tags:** `BE`, `API`
* **Descrição:** Criar o endpoint `POST /api/reports/{id}/flag` que permite a um usuário autenticado sinalizar um relato, registrando o motivo e o ID do autor da sinalização.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A funcionalidade opera conforme o esperado no ambiente de testes.
    * ✅ A documentação da API foi atualizada.

<br>

**Card 6: UI para sinalização de relatos**
* **História Relacionada:** HU-CID-005
* **Tags:** `FE`, `UI`
* **Descrição:** Na tela de detalhes de um relato, implementar o botão/menu que abre um modal para o usuário selecionar o motivo da sinalização e enviar para a API.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A interface funciona conforme o design de UI/UX.
    * ✅ A funcionalidade foi testada e validada no ambiente de testes.

---

### **Épico: Cadastro e Gestão de Resgates (ONG)**

<br>

**Card 7: API para visualização e filtragem de ocorrências**
* **História Relacionada:** HU-ONG-002, HU-ONG-003
* **Tags:** `BE`, `API`, `DB`, `Geo`
* **Descrição:** Criar o endpoint `GET /api/reports/open` para retornar uma lista paginada de relatos abertos, com suporte a filtros por tipo de animal, condição e raio de distância (geo-query).
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A funcionalidade opera conforme o esperado no ambiente de testes.
    * ✅ A documentação da API foi atualizada.

<br>

**Card 8: UI do painel de ocorrências da ONG**
* **História Relacionada:** HU-ONG-002, HU-ONG-003
* **Tags:** `FE`, `UI`, `Maps`
* **Descrição:** Desenvolver o painel principal da ONG, com o seletor de visão (Mapa/Lista) e os controles de filtro, exibindo os dados consumidos da API de ocorrências.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A interface funciona conforme o design de UI/UX.
    * ✅ A funcionalidade foi testada e validada no ambiente de testes.

<br>

**Card 9: API para gestão de casos (Assumir, Liberar, Atualizar Status)**
* **História Relacionada:** HU-ONG-004, HU-ONG-006, HU-ONG-007
* **Tags:** `BE`, `API`
* **Descrição:** Desenvolver os endpoints para o ciclo de vida de um caso: `POST /api/reports/{id}/assume`, `POST /api/reports/{id}/status`, `POST /api/reports/{id}/release`.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A funcionalidade opera conforme o esperado no ambiente de testes.
    * ✅ A documentação da API foi atualizada.

<br>

**Card 10: UI da gestão de casos assumidos ("Meus Acolhidos")**
* **História Relacionada:** HU-ONG-005, HU-ONG-006
* **Tags:** `FE`, `UI`
* **Descrição:** Desenvolver a tela "Meus Acolhidos" e a tela de "Detalhes do Caso Assumido", permitindo que a ONG visualize e interaja com os casos sob sua responsabilidade.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A interface funciona conforme o design de UI/UX.
    * ✅ A funcionalidade foi testada e validada no ambiente de testes.

---

### **Épico: Governança e Moderação da Plataforma (Admin)**

<br>

**Card 11: API para administração e moderação**
* **História Relacionada:** HU-ADM-001, HU-ADM-002, HU-ADM-003, HU-ADM-004, HU-ADM-005
* **Tags:** `BE`, `API`, `Admin`
* **Descrição:** Desenvolver os endpoints restritos para administradores, incluindo a listagem de ONGs pendentes, as ações de aprovar/rejeitar, a listagem de relatos sinalizados e as ações de manter/excluir.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A funcionalidade opera conforme o esperado no ambiente de testes.
    * ✅ A documentação da API foi atualizada.

<br>

**Card 12: UI do painel do administrador**
* **História Relacionada:** HU-ADM-001, HU-ADM-002, HU-ADM-003, HU-ADM-004, HU-ADM-005
* **Tags:** `FE`, `UI`, `Admin`
* **Descrição:** Desenvolver a interface do painel de administração com as seções "Aprovação de ONGs" e "Moderação de Conteúdo", integrando com os respectivos endpoints da API.
* **Definition of Done (DoD):**
    * ✅ O código foi revisado e aprovado por outro desenvolvedor.
    * ✅ A interface funciona conforme o design de UI/UX.
    * ✅ A funcionalidade foi testada e validada no ambiente de testes.

---

## Estrutura e convenções do quadro Kanban

### Definição das TAGs

As tags são usadas para categorizar o tipo de trabalho em cada card, facilitando a visualização e a organização do fluxo.

| TAG | Nome Descritivo | Descrição Breve |
| :--- | :--- | :--- |
| `FE` | Frontend | Tarefas relacionadas à interface do usuário no aplicativo móvel. |
| `BE` | Backend | Tarefas relacionadas à lógica do servidor, regras de negócio e APIs. |
| `DB` | Banco de Dados | Tarefas que envolvem a modelagem, criação ou migração de tabelas. |
| `API`| API | Tarefas focadas na criação ou modificação de endpoints. |
| `UI` | User Interface | Tarefas de desenvolvimento visual e de componentes de tela. |
| `Auth`| Autenticação | Tarefas relacionadas ao fluxo de login, cadastro e segurança de acesso. |
| `Geo` | Geolocalização | Tarefas que envolvem lógica de dados espaciais (ex: PostGIS). |
| `Maps`| Mapas | Tarefas relacionadas à integração e exibição de mapas na interface. |
| `Mobile`| Mobile | Tarefas específicas do ambiente móvel (ex: acesso a hardware nativo). |
| `Admin`| Administrativo | Tarefas relacionadas ao painel de administração da plataforma. |

---

## Estrutura do quadro Kanban e automações

| Coluna / Raia | Propósito | Automação Sugerida (Trello + GitHub) |
| :--- | :--- | :--- |
| **BACKLOG** | Contém todos os cards refinados e priorizados. | - |
| **SPRINT BACKLOG** | A equipe puxa os cards de maior prioridade do Backlog para esta coluna. | - |
| **DESENVOLVIMENTO** | Onde um desenvolvedor está trabalhando ativamente em um card. | Quando um dev se atribui a um card, ele é movido para cá. |
| **REVISÃO** | Um Pull Request (PR) foi aberto. Aguardando a revisão. | **Gatilho:** PR criado no GitHub. **Ação:** Card movido para "REVISÃO". |
| **HOMOLOGAÇÃO**| O PR foi mesclado na branch `staging`/`develop`. | **Gatilho:** PR mesclado na branch `staging`. **Ação:** Card movido para "HOMOLOGAÇÃO". |
| **CONCLUÍDO** | A funcionalidade foi validada e implantada em produção. | **Gatilho:** Código mesclado na branch `main`. **Ação:** Card movido para "CONCLUÍDO". |
