# Sistema de Gestão de Atendimento Acadêmico — Modelagem UML

Trabalho prático da disciplina de **Modelagens de Sistemas em UML** — Universidade Estácio de Sá, Campus Parangaba.

## Integrantes

| Nome 
|------|
| Daniel Sampaio Silva 
| Nicolas Levy Felix Araújo
| João Victor Firmeza Duarte
| Antônio Carlos da Silva Neto
| Pedro Miguel Nascimento da Silva Sousa

---

## Sobre o Projeto

Este trabalho documenta a modelagem UML de um **sistema de gestão de atendimento acadêmico** para Instituições de Ensino Superior (IES).

O problema central é o uso habitual de canais informais (WhatsApp, e-mail) para comunicação acadêmica, o que gera perda de informações, falta de rastreabilidade e sobrecarga administrativa. O sistema proposto centraliza solicitações acadêmicas, controle de presença docente e comunicação entre alunos, professores, secretaria e coordenação.

---


## Diagramas Produzidos

### Diagrama de Caso de Uso
Representa os atores do sistema (Aluno, Professor, Secretaria, Coordenação, Administração) e suas interações com as funcionalidades principais, como registrar solicitação acadêmica e realizar check-in.

### Diagrama de Classes
Modela a estrutura estática do sistema com herança a partir da classe `Pessoa`, controle de acesso baseado em funções (RBAC) e as entidades de negócio como `Solicitacao`, `Disciplina`, `Turma` e `Notificacao`.

### Diagrama de Sequência
Detalha a interação entre objetos no fluxo de **Registrar Solicitação Acadêmica**, mostrando a ordem das mensagens trocadas entre aluno, sistema e banco de dados.

### Diagrama de Estados
Representa o ciclo de vida de uma solicitação acadêmica, passando pelos status: `Aberta → Em Validação → Em Análise → Respondida → Deferida / Indeferida → Concluída / Cancelada`.

---

## Requisitos do Sistema

### Funcionais (principais)
- Cadastro de alunos, professores, disciplinas e turmas
- Registro e acompanhamento de solicitações acadêmicas com anexo de documentos
- Validação pela secretaria e resposta por professor ou coordenação
- Check-in do professor antes da aula com verificação de sala
- Notificações ao aluno sobre o andamento da solicitação
- Escolha do meio de notificação preferido (SMS, e-mail ou push)
- Criação automática de grupos de conversa por disciplina/turma
- Geração de relatórios

### Não Funcionais (principais)
- Sistema web e responsivo
- Autenticação por login e senha
- Banco de dados relacional
- Arquitetura MVC
- Controle de acesso por perfil de usuário
- Tempo de resposta ≤ 3 segundos
- Acessibilidade total
- Criptografia de informações confidenciais

### Regras de Negócio (principais)
- Uma solicitação está vinculada a um único aluno e deve ter um tipo definido
- O aluno não pode alterar a solicitação após ela entrar em análise
- O check-in do professor deve ocorrer antes do horário da aula para validar o ponto
- Status possíveis: `Aberta`, `Em Validação`, `Em Análise`, `Respondida`, `Deferida`, `Indeferida`, `Cancelada`, `Concluída`

---

## Tecnologias e Ferramentas

- **Linguagem de modelagem:** UML (Unified Modeling Language)
- **Ferramenta de diagramação:** PlantUML e draw.io

---

## Status do Trabalho

- [x] Documento de requisitos
- [x] Diagrama de caso de uso
- [x] Diagrama de classes
- [x] Diagrama de sequência
- [x] Diagrama de estados
- [x] Diagrama de atividades
- [x] Diagrama de componentes
- [x] Diagrama de implantação
- [x] Relatório final

---

## Referências

- FRÖHLICH, C.; SILVA, L. P.; VIEGAS, C. V. Análise de aderência ao sistema de autoatendimento de serviços universitários. *Revista de Gestão Universitária*, v. 9, n. 2, 2018.
- VIDIGAL, F.; BARROS, G. L. A avaliação da satisfação de usuários de um sistema de gestão de informações acadêmicas. 2015.
- ROUIBAH, K. et al. Critical success factors affecting information system satisfaction in public sector organizations. *Journal of Global Information Management*, v. 28, n. 3, 2020.