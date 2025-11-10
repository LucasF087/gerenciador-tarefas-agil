
---

# 📘 Documentação Teórica – Projeto AgilTaskFlow

---

# 1. Visão Geral do Projeto

---

## 🎯 Objetivo Principal

O AgilTaskFlow foi desenvolvido com a proposta de facilitar o gerenciamento de tarefas de forma enxuta, prática e organizada.

O sistema permite criar, listar, editar e excluir atividades, aplicando na prática conceitos aprendidos em Engenharia de Software, com foco em metodologias ágeis, versionamento e boas práticas profissionais de desenvolvimento.

---

## 📋 Escopo do Sistema

O projeto implementa um CRUD completo de tarefas, com armazenamento em arquivo JSON. Cada tarefa possui:

- Título
- Descrição
- Status

✅ Prioridade (feature incluída como ampliação de escopo durante o desenvolvimento)

✅ As interações podem ser realizadas via CLI ou API utilizando Flask.

---

# 2. Abordagem Aplicada

---

## 🧩 Metodologia Ágil Estruturada

Foi utilizada uma abordagem híbrida baseada em Kanban, utilizando o GitHub Projects como ferramenta visual de fluxo de trabalho. Foram definidas três colunas principais:

- To Do (A Fazer)
- In Progress (Em Progresso)
- Done (Concluído)

Cada cartão do quadro representou entregáveis reais do projeto, como: implementação, testes, documentação, CI/CD, estruturação do vídeo final, entre outros.

---

# 3. Construção do Código

---

## ❗️ Importância da Modelagem

Antes da construção do código, a modelagem contribuiu para estruturar melhor requisitos e alinhamento sobre o comportamento esperado do sistema. Os diagramas UML facilitaram:

- Clareza funcional;
- Comunicação entre desenvolvedores;
- Base para evolução e manutenção futura.

---

# 4. Diagramas UML

---

## 📊 Diagrama de Casos de Uso

Representa o relacionamento entre o usuário e o sistema:

@startuml
actor "Usuário" as U

rectangle "Gerenciador de Tarefas" {
  usecase "Criar Tarefa" as CT
  usecase "Listar Tarefas" as LT
  usecase "Editar Tarefa" as ET
  usecase "Excluir Tarefa" as XT
  usecase "Atribuir Prioridade" as PT
}

U --> CT
U --> LT
U --> ET
U --> XT
U --> PT

@enduml

---

## 📊 Diagrama de Classes

Mostra a organização estrutural das principais classes do sistema:

@startuml
class Task {
  id: int
  title: str
  description: str
  status: str
  priority: str

  to_dict(): dict
}

class TaskManager {
  tasks: list

  load_tasks(): None
  save_tasks(): None
  add_task(task: Task): None
  update_task(id: int, **kwargs): None
  delete_task(id: int): None
  list_tasks(): list
}

TaskManager "1" *-- "many" Task

@enduml

---

# 5. Mudança de Escopo

---

## 🔄 Atualização do Plano

Durante o desenvolvimento, foi adicionada a funcionalidade de prioridade, simulando evolução natural de requisito em ambiente ágil. Essa mudança demandou:

- Atualização da classe Task;
- Ajustes nas funções de CRUD;
- Criação de testes adicionais (test_tasks_extra.py);
- Novos commits semânticos e card de mudança registrado no Kanban.

---

# 6. Testes Automatizados

---

## 🧪 Integração Contínua

Os testes foram escritos em Pytest para validar o funcionamento correto do CRUD com persistência.
Eles asseguram o comportamento esperado nas rotinas de criação, edição, exclusão, tratamento de erros e funcionamento da funcionalidade de prioridade, onde os testes foram integrados ao GitHub Actions, assegurando CI/CD contínuo e qualidade de entrega.

---

# 7. Evidências do GitHub

---

## 🧾 Registro de Dados 

- Kanban organizado em To Do → In Progress → Done
- Mais de 10 commits semânticos registrados
- Workflows executados com sucesso (GitHub Actions)

- Arquivo de evidências saved em:

📎 **/docs/prints/Sucesso - 2 Workflows Runs - LucasF.png**

---

# 8. Conclusão

---

O AgilTaskFlow sintetiza, de forma prática e aplicada, os conceitos fundamentais da Engenharia de Software moderna. 

Tendo uma modelagem estruturada, planejamento ágil, implementação iterativa, testes automatizados, CI/CD, documentação e entrega final — o ciclo completo de desenvolvimento profissional foi colocado em prática de ponta a ponta.

---

# 👨‍💻 Autor

---

**Lucas Ferreira da Silva**

**Projeto desenvolvido como parte da disciplina de Software Engineering - EAD**

**Trabalho referente ao 3º Semestre do curso de Engenharia da Computação — UniFECAF**

**© 2025 — Todos os direitos reservados.**

---