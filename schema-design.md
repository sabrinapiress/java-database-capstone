## 🗄️ Projeto do Banco de Dados MySQL

### Tabela: pacientes
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `nome` VARCHAR(100) NOT NULL  
- `data_nascimento` DATE NOT NULL  
- `email` VARCHAR(100) UNIQUE NOT NULL  
- `telefone` VARCHAR(15)  

### Tabela: medicos
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `nome` VARCHAR(100) NOT NULL  
- `especialidade` VARCHAR(100)  
- `email` VARCHAR(100) UNIQUE NOT NULL  

### Tabela: agendamentos
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `paciente_id` INT NOT NULL FOREIGN KEY REFERENCES pacientes(id)  
- `medico_id` INT NOT NULL FOREIGN KEY REFERENCES medicos(id)  
- `data_agendamento` DATETIME NOT NULL  
- `status` VARCHAR(50) DEFAULT 'agendado'  

### Tabela: administradores
- `id` INT PRIMARY KEY AUTO_INCREMENT  
- `usuario` VARCHAR(50) UNIQUE NOT NULL  
- `senha_hash` VARCHAR(255) NOT NULL  
- `papel` VARCHAR(50) NOT NULL  

---

## 📄 Projeto da Coleção MongoDB

### Coleção: prescricoes

```json
{
  "prescricao_id": "RX123456",
  "paciente_id": 101,
  "medico_id": 202,
  "data_emissao": "2025-08-01T10:30:00Z",
  "medicamentos": [
    {
      "nome": "Amoxicilina",
      "dosagem": "500mg",
      "frequencia": "3 vezes ao dia",
      "duracao": "7 dias"
    },
    {
      "nome": "Ibuprofeno",
      "dosagem": "200mg",
      "frequencia": "quando necessário",
      "duracao": "5 dias"
    }
  ],
  "observacoes": "O paciente deve evitar álcool durante o tratamento."
}
