# 📘 Documentação Teórica – Projeto Gerenciador de Tarefas Ágil

## 1. Descrição do Projeto

### 🎯 Objetivo
O sistema tem como objetivo **gerenciar tarefas de forma simples e eficiente**, permitindo criar, listar, atualizar e excluir atividades.  
Ele foi desenvolvido como parte do trabalho de **Engenharia de Software**, aplicando **metodologias ágeis** e **boas práticas de desenvolvimento**.

### 📋 Escopo
O sistema implementa um **CRUD completo de tarefas**, com armazenamento em arquivo `JSON`.  
Cada tarefa contém:
- **Título**
- **Descrição**
- **Status**
- **Prioridade** (feature adicionada como mudança de escopo)

As tarefas podem ser manipuladas por uma interface simples (CLI ou via API Flask).

### ⚙️ Metodologia Ágil
Foi utilizada uma metodologia **híbrida baseada em Kanban**, com o quadro organizado no GitHub Projects.  
O fluxo inclui as colunas:
- **To Do (A Fazer)**
- **In Progress (Em Progresso)**
- **Done (Concluído)**

Cada card representa uma etapa do projeto (planejamento, código, testes, CI/CD, documentação, vídeo, etc.).

---

## 2. Importância da Modelagem

A modelagem é essencial para garantir a **clareza estrutural e funcional** do sistema antes da implementação.  
O uso de **diagramas UML** facilita:
- A compreensão dos requisitos.
- A comunicação entre desenvolvedores.
- A manutenção e evolução do sistema.

---

## 3. Diagramas UML

### 🔹 Diagrama de Casos de Uso
Representa a interação entre o usuário e o sistema.

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

### 🔹 Diagrama de Classes
Mostra a estrutura das classes principais.

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

## 4. Mudança de Escopo

Durante o desenvolvimento, foi adicionada a funcionalidade de **prioridade nas tarefas**.  
Essa feature surgiu como forma de **melhorar a organização** e simular uma mudança de requisitos em ambiente ágil.  
A alteração envolveu:
- Atualização do modelo `Task`.
- Ajuste nas funções de CRUD.
- Atualização dos testes (`test_tasks_extra.py`).
- Novo commit e card criado no Kanban.

---

## 5. Testes Automatizados

Os testes foram desenvolvidos com **Pytest** e garantem o correto funcionamento do CRUD.  
Eles validam:
- Criação e persistência de tarefas.
- Edição e exclusão de tarefas.
- Tratamento de erros (ex.: ID inexistente).
- A nova funcionalidade de prioridade.

Os testes são executados automaticamente via **GitHub Actions**, garantindo a **integração contínua (CI/CD)** e a qualidade do código.

---

## 6. Prints do GitHub (Evidências)

- ✅ **Kanban Project**: organizado em *To Do*, *In Progress* e *Done*.
- ✅ **Commits**: mais de 10 commits semânticos.
- ✅ **Workflow GitHub Actions**: todos os testes passaram com sucesso.  
  Print salvo em:

/docs/prints/Sucesso - 2 Workflows Runs - LucasF.png

---

## 7. Conclusão

O projeto “**Gerenciador de Tarefas Ágil**” demonstra o uso prático dos conceitos de **Engenharia de Software** e **Metodologias Ágeis**, integrando:
- Planejamento iterativo.
- Modelagem UML.
- Testes automatizados.
- Integração contínua.
- Documentação teórica.

Esses elementos juntos refletem o ciclo completo de desenvolvimento de software profissional e garantem qualidade, confiabilidade e manutenção futura.

---

📅 **Autor:** Lucas Ferreira da Silva  
🏫 **Curso:** Engenharia de Software — Unifecaf  
🧩 **Disciplina:** Software Engineering