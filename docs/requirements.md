# Requisitos Funcionais e Regras de Negócio

Este documento detalha os requisitos funcionais da plataforma "PetHelp", com base nas definições de UI/UX.

---

### Perfis de Usuário

- **Cidadão:** Usuário geral que pode registrar ocorrências.
- **ONG:** Organização verificada que pode visualizar e gerenciar ocorrências.
- **Administrador (Admin):** Usuário com permissões para gerenciar ONGs e moderar conteúdo.

---

### Funcionalidades Globais

#### 1. Cadastro e Autenticação

- **RG-001:** O sistema deve permitir cadastro via E-mail/Senha e via provedor social (Google).
- **RG-002:** A tela de cadastro deve apresentar a escolha clara entre os perfis "Cidadão" e "ONG".
- **RG-003:** O cadastro de "Cidadão" deve ser simples (Nome, E-mail, Senha) e garantir acesso imediato.
- **RG-004:** O cadastro de "ONG" deve solicitar dados para verificação (Nome da ONG, CNPJ, Responsável, Contato).
- **RG-005:** Contas de ONG recém-cadastradas devem ter o status "Pendente de Aprovação" e não podem acessar as funcionalidades de gestão até serem aprovadas por um Admin.

---

### Funcionalidades do Perfil "Cidadão"

#### 2. Tela Inicial e Acesso

- **RG-006:** O aplicativo deve abrir em uma tela inicial focada na ação principal "Registrar Animal", sem forçar login (Acesso Progressivo).
- **RG-007:** O usuário pode realizar um registro completo sem estar logado.

#### 3. Registro de Ocorrência

- **RG-008:** O formulário de registro deve ter acesso à câmera do dispositivo para capturar uma foto do animal.
- **RG-009:** O registro deve capturar automaticamente a localização GPS do usuário no momento do relato.
- **RG-010:** O formulário deve conter os campos pré-definidos "Tipo de Animal" e "Condição", com opções de múltipla escolha.
- **RG-011:** O formulário deve conter um campo de texto livre para "Observações".

---

### Funcionalidades do Perfil "ONG"

#### 4. Painel de Ocorrências

- **RG-012:** A ONG deve ter acesso a um painel com a visualização de ocorrências em formato de Mapa e Lista.
- **RG-013:** A visão de mapa deve agrupar pins próximos (clustering) para evitar poluição visual.
- **RG-014:** O sistema deve permitir filtrar as ocorrências por Proximidade, Tipo de Animal e Condição.
- **RG-015:** Ao selecionar uma ocorrência, a ONG pode visualizar todos os detalhes e tem a opção de "Assumir Resgate".

#### 5. Gestão de Casos Assumidos ("Meus Acolhidos")

- **RG-016:** A ONG deve ter uma área "Meus Acolhidos" listando apenas os casos sob sua responsabilidade.
- **RG-017:** Um caso assumido deve ter um status (Ex: "Aguardando Resgate", "Em Tratamento", "Concluído").
- **RG-018:** Apenas a ONG que assumiu um caso pode alterar seu status.
- **RG-019:** A ONG deve poder "Liberar um Caso", que o devolverá à lista pública de ocorrências.
- **RG-020:** O sistema deve manter um histórico de atualizações para cada caso assumido.

---

### Funcionalidades do Perfil "Administrador"

#### 6. Gestão de ONGs

- **RG-021:** O Admin deve ter acesso a um painel que lista todas as ONGs com status "Pendente de Aprovação".
- **RG-022:** O Admin deve ter as ações de "Aprovar" ou "Rejeitar" cada solicitação de cadastro de ONG.

#### 7. Moderação de Conteúdo

- **RG-023:** Qualquer usuário (Cidadão ou ONG) pode "Sinalizar" um relato por motivos pré-definidos (Falso, Duplicado, Inapropriado).
- **RG-024:** Um relato que atinge um número X de sinalizações é automaticamente ocultado da visão pública e movido para uma fila de moderação.
- **RG-025:** O Admin deve ter acesso a uma "Fila de Moderação" com os relatos sinalizados.
- **RG-026:** O Admin deve ter as ações de "Manter Relato" (revertendo a ocultação) ou "Excluir Relato".

---

[↩️ Voltar ao README Principal](../README.md)
