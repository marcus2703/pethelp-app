# Relatório de UI/UX: Moderação de Conteúdo

### **Objetivo**

Projetar um sistema de moderação de conteúdo que seja escalável, justo e seguro, utilizando a vigilância da comunidade para sinalizar problemas e o julgamento de Administradores para a decisão final.

---

### **Princípios fundamentais**

1.  **Poder na comunidade:** Empoderar qualquer usuário a sinalizar conteúdo problemático, criando um sistema de auto-regulação.
2.  **Prevenção automatizada:** Utilizar regras simples (como um limite de sinalizações) para ocultar automaticamente conteúdo potencialmente problemático, protegendo a integridade do feed principal.
3.  **Controle centralizado:** Manter a autoridade final de aprovação ou exclusão com a equipe de Administradores, garantindo consistência e evitando abusos.

---

### **Componente 1: A funcionalidade de "Sinalizar" para usuários**

Esta funcionalidade deve ser discreta, mas acessível em todos os relatos.

-   **Gatilho:** Em cada tela de "Detalhes da Ocorrência", haverá um ícone (bandeira 🚩) ou um menu de três pontos (⋮) com a opção "Sinalizar Relato".
-   **Fluxo:**
    1.  O usuário clica em "Sinalizar".
    2.  Abre uma pequena janela (modal) perguntando o motivo.
    3.  O usuário seleciona uma opção pré-definida:
        - `[ ] Relato Falso / Spam`
        - `[ ] Relato Duplicado`
        - `[ ] Conteúdo Ofensivo / Inapropriado`
        - `[ ] O animal não está mais no local / Caso resolvido`
    4.  Após a escolha, o sistema agradece e registra a sinalização. Para o usuário, o processo termina aqui.

#### **Esboço da interação de "Sinalizar"**

```
+-------------------------------------------+
| < Voltar | Detalhes da Ocorrência     (⋮)| <-- Clique aqui
+-------------------------------------------+
|                                           |
|  [Foto do Animal]                         |
|  Cão, Ferido                              |
|  📍 Rua das Flores, 123                   |
|  Obs: "..."                               |
|                   +---------------------+ |
|                   |   Sinalizar Relato  | |
|                   +---------------------+ |
+-------------------------------------------+
```

---

### **Componente 2: A fila de moderação para ADMINs**

Esta é a nova ferramenta de trabalho no painel do Administrador.

-   **Acesso:** Uma nova aba ou seção no painel de Admin chamada "Moderação".
-   **Layout:** Uma lista de cards, similar à de aprovação de ONGs, mas para relatos sinalizados.
-   **Informações no card:** Cada card deve fornecer todo o contexto necessário para a decisão do ADMIN.
    -   As informações do relato original (foto, tipo, condição, etc.).
    -   **Motivo da Sinalização:** Um resumo de quantas vezes e por quais motivos o relato foi sinalizado (Ex: "Sinalizado 3 vezes: 2x Falso, 1x Duplicado").
-   **Ações no card:** Botões claros para a decisão final.
    -   **[✔] MANTER RELATO:** Ignora as sinalizações e torna o relato público novamente, caso tenha sido ocultado.
    -   **[✖] EXCLUIR RELATO:** Remove permanentemente o relato da plataforma. Exige uma confirmação.

#### **Esboço do painel de moderação do ADMIN**

```
+-------------------------------------------+
| ☰ Menu | Admin  [Aprovar ONGs][Moderação] |
+-------------------------------------------+
|                                           |
|  Relatos Sinalizados para Revisão (2)     |
|                                           |
+-------------------------------------------+
|                                           |
|  +-------------------------------------+  |
|  | Relato: Cão, Agressivo              |  |
|  | Autor: usuario123@email.com         |  |
|  | Sinalizações: 4                     |  |
|  | Motivos: 3x Falso, 1x Inapropriado  |  |
|  |                                     |  |
|  |  [ Ver Relato ]                     |  |
|  |   [ Manter ]       [ Excluir ]      |  |
|  +-------------------------------------+  |
|                                           |
+-------------------------------------------+
```
---

[↩️ Voltar ao README Principal](../../README.md)
