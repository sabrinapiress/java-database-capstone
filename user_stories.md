# User Story Template

---

**Title:** Administrador - Gerenciar contas de usuários  
_Como administrador, desejo criar e gerenciar contas de usuários para poder controlar o acesso ao sistema._

**Acceptance Criteria:**
1. O administrador pode criar novas contas para médicos e pacientes.
2. O administrador pode editar ou desativar contas existentes.
3. O administrador pode visualizar uma lista de todos os usuários.

**Priority:** Alta  
**Story Points:** 5  
**Notes:**
- Deve haver validação de dados obrigatórios e verificação de duplicidade de e-mail.

---

**Title:** Paciente - Agendar consultas  
_Como paciente, desejo marcar consultas com médicos para poder receber cuidados médicos._

**Acceptance Criteria:**
1. O paciente pode visualizar a disponibilidade dos médicos.
2. O paciente pode selecionar data e horário para a consulta.
3. O paciente recebe confirmação da consulta agendada.

**Priority:** Alta  
**Story Points:** 5  
**Notes:**
- O sistema deve impedir agendamentos duplicados.

---

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
