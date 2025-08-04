# User Story

---
# Administrador

**Title:** Administrador - Login no portal
_Como administrador, eu quero fazer login no portal com nome de usuário e senha, e então gerenciar a plataforma com segurança_
**Acceptance Criteria:**
1. O administrador pode inserir nome de usuário e senha válidos.
2. O sistema valida as credenciais e permite o acesso.
3. O administrador é redirecionado para o painel principal após login bem-sucedido.
**Priority:** Alta
**Story Points:** 3
**Notes:**
- Deve haver tratamento de erros para login inválido.

---

**Title:** Administrador - Logout do portal
_Como administrador, eu quero sair do portal, e então proteger o acesso ao sistema_
**Acceptance Criteria:**
1. O administrador pode clicar em 'Sair' no menu.
2. O sistema encerra a sessão atual.
3. O administrador é redirecionado para a tela de login.
**Priority:** Alta
**Story Points:** 2
**Notes:**
- Sessões devem expirar automaticamente após inatividade.

---

**Title:** Administrador - Adicionar médicos
_Como administrador, eu quero adicionar médicos ao portal, e então permitir que médicos utilizem o sistema_
**Acceptance Criteria:**
1. O administrador pode preencher dados do médico.
2. O sistema valida e salva os dados.
3. O novo médico aparece na lista de usuários.
**Priority:** Alta
**Story Points:** 4
**Notes:**
- Deve haver verificação de duplicidade de e-mail.

---

**Title:** Administrador - Excluir perfil de médico
_Como administrador, eu quero excluir perfil de médico do portal, e então remover acesso de médicos inativos_
**Acceptance Criteria:**
1. O administrador pode selecionar um médico e clicar em 'Excluir'.
2. O sistema solicita confirmação.
3. O perfil é removido da base de dados.
**Priority:** Média
**Story Points:** 3
**Notes:**
- Perfis excluídos devem ser arquivados antes da remoção.

---

**Title:** Administrador - Executar procedimento MySQL
_Como administrador, eu quero executar procedimento armazenado na CLI do MySQL, e então obter número de compromissos por mês e acompanhar estatísticas_
**Acceptance Criteria:**
1. O administrador acessa a CLI do MySQL.
2. Executa o procedimento armazenado com sucesso.
3. Recebe os dados estatísticos mensais de compromissos.
**Priority:** Alta
**Story Points:** 5
**Notes:**
- Procedimento deve estar documentado e seguro.

---

#

# Paciente

**Title:** Paciente - Visualizar lista de médicos sem login  
_Como paciente, quero ver uma lista de médicos disponíveis sem fazer login, para que eu possa explorar as opções antes de me registrar._

**Acceptance Criteria:**
1. O sistema exibe uma lista de médicos disponíveis sem exigir login.
2. A lista inclui especialidade, nome e disponibilidade.
3. O paciente pode clicar para ver mais detalhes do médico.

**Priority:** Média  
**Story Points:** 3  
**Notes:**
- A lista deve ser atualizada automaticamente com base na disponibilidade.

---

**Title:** Paciente - Cadastro com e-mail e senha  
_Como paciente, desejo me cadastrar usando meu e-mail e senha para poder agendar consultas._

**Acceptance Criteria:**
1. O paciente pode preencher um formulário de cadastro com e-mail e senha.
2. O sistema valida os dados e cria uma conta.
3. O paciente recebe confirmação de cadastro.

**Priority:** Alta  
**Story Points:** 5  
**Notes:**
- Deve haver verificação de duplicidade de e-mail.

---

**Title:** Paciente - Login no portal para gerenciar reservas  
_Como paciente, desejo fazer login no portal para poder gerenciar minhas reservas._

**Acceptance Criteria:**
1. O paciente pode acessar o portal com e-mail e senha.
2. O sistema exibe as consultas agendadas.
3. O paciente pode cancelar ou reagendar consultas.

**Priority:** Alta  
**Story Points:** 5  
**Notes:**
- Sessão deve expirar após inatividade.

---

**Title:** Paciente - Logout do portal  
_Como paciente, desejo sair do portal para poder proteger minha conta._

**Acceptance Criteria:**
1. O paciente pode clicar em “Sair” para encerrar a sessão.
2. O sistema redireciona para a página inicial.
3. A sessão é encerrada com segurança.

**Priority:** Média  
**Story Points:** 2  
**Notes:**
- Deve haver confirmação visual de logout.

---

**Title:** Paciente - Marcar consulta de uma hora  
_Como paciente, desejo marcar uma consulta de uma hora com um médico, para poder receber atendimento médico._

**Acceptance Criteria:**
1. O paciente pode selecionar médico, data e horário.
2. O sistema verifica disponibilidade e confirma agendamento.
3. O paciente recebe notificação da consulta marcada.

**Priority:** Alta  
**Story Points:** 5  
**Notes:**
- Deve haver limite de uma consulta por médico por horário.

#

# Médico

**Title:** Médico - Definir disponibilidade  
_Como médico, quero definir meus horários disponíveis para que os pacientes possam marcar consultas de acordo._

**Acceptance Criteria:**
1. O médico pode adicionar horários disponíveis.
2. O médico pode editar ou remover horários.
3. Os pacientes só podem agendar dentro dos horários definidos.

**Priority:** Média  
**Story Points:** 3  
**Notes:**
- Deve haver verificação de conflitos com consultas já agendadas.

# Histórias de Usuário - Médico

**Title:** Médico - Login no portal  
_Como médico, quero fazer login no portal, para poder gerenciar meus compromissos._

**Acceptance Criteria:**
1. O médico pode acessar o portal com e-mail e senha válidos.
2. O sistema valida credenciais e redireciona para o painel médico.
3. Mensagens de erro são exibidas em caso de falha no login.

**Priority:** Alta  
**Story Points:** 3  
**Notes:**  
- O login deve ser protegido por autenticação segura.

---

**Title:** Médico - Logout do portal  
_Como médico, quero sair do portal, para proteger meus dados._

**Acceptance Criteria:**
1. O médico pode clicar em 'Sair' para encerrar a sessão.
2. A sessão é finalizada e o usuário é redirecionado à página inicial.
3. Nenhum dado sensível permanece acessível após logout.

**Priority:** Alta  
**Story Points:** 2  
**Notes:**  
- O logout deve funcionar em todos os navegadores.

---

**Title:** Médico - Exibir calendário de compromissos  
_Como médico, quero ver meu calendário de compromissos, para que eu me mantenha organizado._

**Acceptance Criteria:**
1. O médico pode visualizar compromissos futuros e passados.
2. Os compromissos são exibidos com data, hora e nome do paciente.
3. O calendário permite navegação por mês e semana.

**Priority:** Alta  
**Story Points:** 4  
**Notes:**  
- O calendário deve ser responsivo e fácil de usar.

---

**Title:** Médico - Marcar indisponibilidade  
_Como médico, quero marcar horários indisponíveis, para que informe aos pacientes apenas os slots disponíveis._

**Acceptance Criteria:**
1. O médico pode selecionar datas e horários como indisponíveis.
2. Esses horários não aparecem para agendamento por pacientes.
3. O sistema impede agendamento em horários bloqueados.

**Priority:** Média  
**Story Points:** 3  
**Notes:**  
- Deve haver confirmação visual dos horários bloqueados.

---

**Title:** Médico - Atualizar perfil  
_Como médico, desejo atualizar informações de especialização e contato, para que os pacientes tenham informações atualizadas._

**Acceptance Criteria:**
1. O médico pode editar especialidade, telefone e e-mail.
2. As alterações são salvas e refletidas no perfil público.
3. O sistema valida os campos antes de salvar.

**Priority:** Média  
**Story Points:** 3  
**Notes:**  
- O perfil deve ser atualizado em tempo real.

---

**Title:** Médico - Visualizar detalhes do paciente  
_Como médico, quero ver detalhes do paciente para consultas futuras, para que esteja preparado para o atendimento._

**Acceptance Criteria:**
1. O médico pode acessar informações do paciente agendado.
2. Os dados incluem histórico médico e prescrições anteriores.
3. O acesso é restrito aos pacientes com consulta marcada.

**Priority:** Alta  
**Story Points:** 4  
**Notes:**  
- Deve haver controle de acesso seguro aos dados.


