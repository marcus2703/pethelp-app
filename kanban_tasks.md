# Backlog de Tarefas para o Quadro Kanban

Este documento detalha as tarefas de desenvolvimento prontas para a equipe, alinhadas com as Histórias de Usuário e formatadas como cards para o Kanban.

---

### **Épico: Engajamento e Relato (Cidadão)**

<br>

**Card 1: API para Submissão de Relatos**
* **História Relacionada:** HU-CID-001, HU-CID-003
* **Tags:** `BE`, `API`
* **Descrição:** Construir e testar o endpoint `POST /api/reports` que recebe os dados de um novo relato (incluindo a imagem), valida as informações e as persiste no banco de dados, retornando uma resposta de sucesso.
* **Checklist de Tarefas:**
    * [ ] Definir a rota e o controller para `POST /api/reports`.
    * [ ] Implementar a validação do corpo da requisição (payload).
    * [ ] Integrar com o serviço de upload de imagens.
    * [ ] Criar o serviço para salvar os dados na tabela `reports`.
* **Definition of Done (DoD):**
    * ✅ Código revisado (PR aprovado).
    * ✅ Testes de unidade cobrem os fluxos de sucesso e erro.
    * ✅ Endpoint documentado no Postman/Swagger.
    * ✅ Validado em ambiente de Staging.

<br>

**Card 2: UI da Tela de Novo Relato**
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
    * ✅ Código revisado (PR aprovado).
    * ✅ Componente funciona conforme o protótipo de UI/UX.
    * ✅ Integração com a API validada em Staging.

<br>

**Card 3: API para Autenticação e Cadastro de Usuários**
* **História Relacionada:** HU-CID-002, HU-ONG-001
* **Tags:** `BE`, `API`, `Auth`
* **Descrição:** Implementar os endpoints `POST /api/auth/register` e `POST /api/auth/login` para o cadastro e autenticação de usuários (Cidadão e ONG), retornando um token JWT.
* **Checklist de Tarefas:**
    * [ ] Modelar a tabela `users` com campos para perfil (role), status, etc.
    * [ ] Implementar a lógica de hashing de senhas.
    * [ ] Criar o endpoint de registro, validando os dados de entrada.
    * [ ] Criar o endpoint de login, validando as credenciais.
* **Definition of Done (DoD):** Ver DoD padrão do Backend.

<br>

**Card 4: UI das Telas de Login e Cadastro**
* **História Relacionada:** HU-CID-002, HU-ONG-001
* **Tags:** `FE`, `UI`, `Auth`
* **Descrição:** Desenvolver as telas de Login, a tela de escolha de perfil ("Cidadão" ou "ONG"), e os respectivos formulários de cadastro, integrando-os com a API de autenticação.
* **Checklist de Tarefas:**
    * [ ] Criar a tela de Login e a tela de Pré-Cadastro.
    * [ ] Desenvolver o formulário de cadastro simples para Cidadão.
    * [ ] Desenvolver o formulário de cadastro detalhado para ONG.
    * [ ] Integrar os formulários com os endpoints da API de autenticação.
* **Definition of Done (DoD):** Ver DoD padrão do Frontend.

<br>

**Card 5: API para Sinalização de Relatos**
* **História Relacionada:** HU-CID-005
* **Tags:** `BE`, `API`
* **Descrição:** Criar o endpoint `POST /api/reports/{id}/flag` que permite a um usuário autenticado sinalizar um relato, registrando o motivo e o ID do autor da sinalização.
* **Definition of Done (DoD):** Ver DoD padrão do Backend.

<br>

**Card 6: UI para Sinalização de Relatos**
* **História Relacionada:** HU-CID-005
* **Tags:** `FE`, `UI`
* **Descrição:** Na tela de detalhes de um relato, implementar o botão/menu que abre um modal para o usuário selecionar o motivo da sinalização e enviar para a API.
* **Definition of Done (DoD):** Ver DoD padrão do Frontend.

---

### **Épico: Cadastro e Gestão de Resgates (ONG)**

<br>

**Card 7: API para Visualização e Filtragem de Ocorrências**
* **História Relacionada:** HU-ONG-002, HU-ONG-003
* **Tags:** `BE`, `API`, `DB`, `Geo`
* **Descrição:** Criar o endpoint `GET /api/reports/open` para retornar uma lista paginada de relatos abertos, com suporte a filtros por tipo de animal, condição e raio de distância (geo-query).
* **Definition of Done (DoD):** Ver DoD padrão do Backend.

<br>

**Card 8: UI do Painel de Ocorrências da ONG**
* **História Relacionada:** HU-ONG-002, HU-ONG-003
* **Tags:** `FE`, `UI`, `Maps`
* **Descrição:** Desenvolver o painel principal da ONG, com o seletor de visão (Mapa/Lista) e os controles de filtro, exibindo os dados consumidos da API de ocorrências.
* **Definition of Done (DoD):** Ver DoD padrão do Frontend.

<br>

**Card 9: API para Gestão de Casos (Assumir, Liberar, Atualizar Status)**
* **História Relacionada:** HU-ONG-004, HU-ONG-006, HU-ONG-007
* **Tags:** `BE`, `API`
* **Descrição:** Desenvolver os endpoints para o ciclo de vida de um caso: `POST /api/reports/{id}/assume`, `POST /api/reports/{id}/status`, `POST /api/reports/{id}/release`.
* **Definition of Done (DoD):** Ver DoD padrão do Backend.

<br>

**Card 10: UI da Gestão de Casos Assumidos ("Meus Acolhidos")**
* **História Relacionada:** HU-ONG-005, HU-ONG-006
* **Tags:** `FE`, `UI`
* **Descrição:** Desenvolver a tela "Meus Acolhidos" e a tela de "Detalhes do Caso Assumido", permitindo que a ONG visualize e interaja com os casos sob sua responsabilidade.
* **Definition of Done (DoD):** Ver DoD padrão do Frontend.

---

### **Épico: Governança e Moderação da Plataforma (Admin)**

<br>

**Card 11: API para Administração e Moderação**
* **História Relacionada:** HU-ADM-001, HU-ADM-002, HU-ADM-003, HU-ADM-004, HU-ADM-005
* **Tags:** `BE`, `API`, `Admin`
* **Descrição:** Desenvolver os endpoints restritos para administradores, incluindo a listagem de ONGs pendentes, as ações de aprovar/rejeitar, a listagem de relatos sinalizados e as ações de manter/excluir.
* **Definition of Done (DoD):** Ver DoD padrão do Backend.

<br>

**Card 12: UI do Painel do Administrador**
* **História Relacionada:** HU-ADM-001, HU-ADM-002, HU-ADM-003, HU-ADM-004, HU-ADM-005
* **Tags:** `FE`, `UI`, `Admin`
* **Descrição:** Desenvolver a interface do painel de administração com as seções "Aprovação de ONGs" e "Moderação de Conteúdo", integrando com os respectivos endpoints da API.
* **Definition of Done (DoD):** Ver DoD padrão do Frontend.

---

## Estrutura do Quadro Kanban e Automações

| Coluna / Raia | Propósito | Automação Sugerida (Trello + GitHub) |
| :--- | :--- | :--- |
| **Backlog** | Contém todos os cards refinados e priorizados. | - |
| **To Do (A Fazer)** | A equipe puxa os cards de maior prioridade do Backlog para esta coluna. | - |
| **Doing (Em Andamento)** | Onde um desenvolvedor está trabalhando ativamente em um card. | Quando um dev se atribui a um card, ele é movido para cá. |
| **Code Review (Revisão)** | Um Pull Request (PR) foi aberto. Aguardando a revisão. | **Gatilho:** PR criado no GitHub. **Ação:** Card movido para "Code Review". |
| **Staging (Homologação)**| O PR foi mesclado na branch `staging`/`develop`. | **Gatilho:** PR mesclado na branch `staging`. **Ação:** Card movido para "Staging". |
| **Done (Feito)** | A funcionalidade foi validada e implantada em produção. | **Gatilho:** Código mesclado na branch `main`. **Ação:** Card movido para "Done". |
