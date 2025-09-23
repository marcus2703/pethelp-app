# Relatório de UI/UX: Painel do Administrador

### **Objetivo**

Projetar uma interface de gerenciamento mínima e funcional para o usuário "Administrador", focada na sua única responsabilidade crítica para o MVP: a aprovação de novos cadastros de ONGs.

---

### **Princípios fundamentais**

1.  **Simplicidade e foco:** A tela deve apresentar apenas a informação necessária para a tomada de decisão (aprovar ou rejeitar uma ONG) e nada mais.
2.  **Ação inequívoca:** Os botões de ação devem ser claros e o resultado de suas ações, previsível.
3.  **Segurança por design:** O acesso a este painel é restrito e o design deve refletir sua natureza funcional e de back-office, sem elementos visuais desnecessários.

---

### **Governança do acesso ADMIN**

A função de Administrador é uma permissão concedida manualmente, não sendo um perfil que o usuário possa solicitar ou se cadastrar para obter.

-   **Modelo de atribuição:** A função "Admin" é atribuída diretamente no banco de dados pela equipe técnica do projeto a um usuário de confiança previamente cadastrado.
-   **Acesso ao painel:** Quando um usuário com a função "Admin" faz login, o sistema o redireciona para este painel de administração em vez da tela inicial do cidadão.

---

### **Componente principal: Tela de aprovação de ONGs**

Para o MVP, o painel do administrador consiste em uma única tela: a lista de ONGs pendentes de aprovação.

-   **Layout:** Uma lista simples de "cards", onde cada card representa uma ONG que completou o cadastro e aguarda validação.
-   **Informações no card:** Cada card deve exibir de forma clara todas as informações coletadas no formulário de cadastro da ONG para facilitar a verificação externa (ex: pesquisar o CNPJ).
    -   Nome da ONG
    -   CNPJ
    -   Nome do Responsável
    -   E-mail de Contato
    -   Telefone
    -   Data do Cadastro
-   **Ações no card:** Cada card terá dois botões de ação distintos.
    -   **[✔] APROVAR:** Altera o status da ONG para "Aprovada", liberando seu acesso ao sistema. O card da ONG é removido desta lista.
    -   **[✖] REJEITAR:** Altera o status para "Rejeitada" (ou simplesmente remove o registro). O card também é removido da lista. Uma confirmação é recomendada: *"Tem certeza que deseja rejeitar esta ONG? Esta ação não pode ser desfeita."*

---

### **Esboço conceitual do painel do administrador**
Com certeza. Aqui está o snippet de código apenas com o esboço conceitual (wireframe) do painel do administrador.

```
+-------------------------------------------+
| ☰ Menu  | Painel de Administração         |
+-------------------------------------------+
|                                           |
|  ONGs Pendentes de Aprovação (3)          |
|                                           |
+-------------------------------------------+
|                                           |
|  +-------------------------------------+  |
|  | Nome: Abrigo Anjos de Patas         |  |
|  | CNPJ: 12.345.678/0001-99            |  |
|  | Responsável: Maria Silva            |  |
|  | Email: contato@anjosdepatas.org     |  |
|  | Telefone: (51) 99999-8888           |  |
|  | Data: 22/09/2025                    |  |
|  |                                     |  |
|  |   [ Aprovar ]      [ Rejeitar ]     |  |
|  +-------------------------------------+  |
|                                           |
|  +-------------------------------------+  |
|  | Nome: Causa Animal Feliz            |  |
|  | CNPJ: 98.765.432/0001-11            |  |
|  | ... (demais informações)            |  |
|  |   [ Aprovar ]      [ Rejeitar ]     |  |
|  +-------------------------------------+  |
|                                           |
+-------------------------------------------+
```
---

[↩️ Voltar ao README Principal](../../README.md)
