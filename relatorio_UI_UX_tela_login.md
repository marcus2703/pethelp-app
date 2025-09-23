# Relatório de UI/UX: Tela de Login e Autenticação

### **Objetivo**

Projetar uma tela de login que seja segura, intuitiva e com o mínimo de atrito possível. A tela deve servir tanto para o "Cidadão" que deseja acompanhar seus registros quanto para o "Gestor" que precisa acessar o painel de gerenciamento.

---

### **Princípios fundamentais**

1.  **Clareza acima de tudo:** O usuário deve entender imediatamente como entrar ou, se necessário, como criar uma conta ou recuperar sua senha, sem ambiguidades.
2.  **Múltiplas opções, simplicidade na escolha:** Oferecer métodos de login modernos (como redes sociais) ao lado do tradicional e-mail e senha, permitindo que o usuário escolha o caminho mais confortável para ele.
3.  **Segurança e confiança:** O design deve transmitir profissionalismo e segurança, garantindo ao usuário que seus dados estão protegidos.

---

### **Contexto de acesso**

Esta tela não é a primeira barreira do aplicativo para o cidadão. Ela é acessada através de ações secundárias na tela inicial, como clicar em "Perfil" ou "Meus Registros" (caso o usuário ainda não esteja logado). Para o usuário do tipo Gestor, esta será a porta de entrada principal para o sistema de gerenciamento.

---

### **Design e layout da tela de login**

A tela deve ser limpa, focada и com os seguintes componentes hierarquizados:

1.  **Título e chamada:** Um título claro como "Acesse sua Conta" e um subtítulo amigável como "Que bom ter você de volta!".
2.  **Campos de entrada (Login Tradicional):**
    -   **E-mail:** Campo padrão para entrada de texto com o rótulo claro.
    -   **Senha:** Campo de senha com um ícone que permite ao usuário alternar a visibilidade do que está digitando.
3.  **Link para recuperação de senha:** Um link discreto mas visível: "Esqueci minha senha", posicionado logo abaixo do campo de senha.
4.  **Botão de ação principal (CTA):** Um botão grande, com cor de destaque e texto inequívoco: "ENTRAR".
5.  **Divisor e login social:** Para reduzir o atrito, o login social é a melhor prática. Um divisor visual (uma linha com o texto "ou") separa os métodos, seguido de botões para provedores como o Google.
6.  **Link para cadastro:** Na base da tela, uma frase clara que convida novos usuários a se registrarem, como: "Ainda não tem uma conta? Cadastre-se aqui".

---

### **Esboço conceitual da tela de login (Wireframe)**

```
+-------------------------------------------+
|                                           |
|                [ Logo App ]               |
|                                           |
|             Acesse sua Conta              |
|      Que bom ter você de volta!           |
|                                           |
+-------------------------------------------+
|                                           |
|  E-mail                                   |
|  +-------------------------------------+  |
|  | seuemail@exemplo.com                |  |
|  +-------------------------------------+  |
|                                           |
|  Senha                                    |
|  +-------------------------------------+  |
|  | *********** [👁️]                    |  |
|  +-------------------------------------+  |
|                       Esqueci minha senha |
|                                           |
|          +-----------------------+        |
|          |        ENTRAR         |        |
|          +-----------------------+        |
|                                           |
|     ─────────────── ou ───────────────    |
|                                           |
|        +-------------------------+        |
|        | [G] Entrar com o Google |        |
|        +-------------------------+        |
|                                           |
+-------------------------------------------+
|    Não tem uma conta? Cadastre-se aqui    |
+-------------------------------------------+
```
