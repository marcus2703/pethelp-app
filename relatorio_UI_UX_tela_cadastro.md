# Relatório de UI/UX: Tela de Cadastro e Definição de Funções

### **Objetivo**

Projetar um fluxo de cadastro claro que separe os usuários "Cidadão" e "ONG" desde o início, e definir um processo de validação para garantir a legitimidade das organizações participantes.

---

### **Princípios fundamentais**

1.  **Clareza na escolha:** O usuário deve entender instantaneamente os dois caminhos possíveis e qual deles corresponde ao seu perfil.
2.  **Atrito mínimo para o cidadão:** O cadastro do cidadão deve ser o mais rápido e simples possível para incentivar o reporte de ocorrências.
3.  **Validação para a ONG:** O fluxo da ONG deve coletar informações suficientes para permitir uma verificação manual, garantindo a integridade da plataforma.

---

### **A estratégia do ponto de escolha**

A tela de cadastro funcionará como uma tela de pré-cadastro, cuja função principal é direcionar o usuário para o formulário correto com base em sua identidade. A abordagem com dois botões chamativos é a ideal para essa finalidade.

#### **Fluxo de cadastro - Cidadão**

-   **Escolha:** Usuário clica no botão "Sou Cidadão".
-   **Formulário Simples:** É direcionado para uma tela com poucos campos:
    -   Nome
    -   E-mail
    -   Senha
-   **Acesso Imediato:** Após o preenchimento, a conta é criada e o usuário é logado automaticamente, pronto para usar o app.

#### **Fluxo de cadastro - ONG (com validação)**

-   **Escolha:** Usuário clica no botão "Sou ONG".
-   **Formulário Detalhado:** É direcionado para um formulário mais completo:
    -   Nome da ONG
    -   CNPJ
    -   Nome do Responsável
    -   E-mail de Contato
    -   Telefone
    -   Senha
-   **Feedback Pós-Cadastro:** Após o envio, o usuário não é logado imediatamente. Em vez disso, ele recebe uma mensagem clara de feedback.
    -   **Mensagem Sugerida:** "Obrigado! Recebemos seu cadastro. Nossa equipe fará uma breve análise das informações para garantir a segurança da plataforma. Você receberá um e-mail assim que sua conta for ativada. O processo costuma levar até 48 horas."
-   **Aprovação:** A conta só se torna funcional após a aprovação de um Administrador.

---

### **Esboço conceitual wireframe da tela de escolha (Pré-cadastro)**

```
┌───────────────────────────────────────────┐
│                                           │
│                [ Logo App ]               │
│                                           │
│          Para começar, quem é você?       │
│                                           │
├───────────────────────────────────────────┤
│                                           │
│       ┌───────────────────────────┐       │
│       │                           │       │
│       │      Sou um Cidadão       │       │
│       │  Quero relatar um animal  │       │
│       │      que encontrei.       │       │
│       │                           │       │
│       └───────────────────────────┘       │
│                                           │
│     ┌──────────────────────────────┐      │
│     │                              │      │
│     │ Represento uma ONG ou Abrigo │      │
│     │  Queremos ajudar no resgate e│      │
│     │     cuidado dos animais.     │      │
│     │                              │      │
│     └──────────────────────────────┘      │
│                                           │
├───────────────────────────────────────────┤
│        Já tem uma conta? Entre aqui       │
└───────────────────────────────────────────┘
```
