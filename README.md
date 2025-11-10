[![CI](https://github.com/LucasF087/gerenciador-tarefas-agil/actions/workflows/python-app.yml/badge.svg)](https://github.com/LucasF087/gerenciador-tarefas-agil/actions/workflows/python-app.yml)

---

# 🧠 AgilTaskFlow — Sistema de Gerenciamento de Tarefas Ágil

---

## 🔗 **Repositório oficial:** [github.com/LucasF087/AgilTaskFlow](https://github.com/LucasF087/AgilTaskFlow)

---

O **AgilTaskFlow** é um sistema desenvolvido em **Python** com o objetivo de aplicar, na prática, os conceitos de **Engenharia de Software** e **Metodologias Ágeis**.

O projeto permite o gerenciamento completo de tarefas por meio de um **sistema CRUD** (criar, listar, atualizar e excluir), incorporando boas práticas de desenvolvimento, testes automatizados e integração contínua via GitHub Actions.

---

## 🎯 Objetivo do Projeto

O projeto foi criado para demonstrar a aplicação de práticas ágeis e ferramentas de apoio ao ciclo de desenvolvimento de software, abordando desde a modelagem até a automação de testes e versionamento.

A proposta central é desenvolver uma solução simples e funcional que simule um ambiente real de trabalho com metodologias ágeis — integrando **Kanban**, **controle de versão (Git/GitHub)** e **integração contínua (CI)**.

---

## 📋 Escopo Funcional

O **AgilTaskFlow** oferece as seguintes funcionalidades principais:

- ✅ Criar, listar, editar e excluir tarefas (CRUD completo);  
- 🗂️ Armazenamento local em formato **JSON**;  
- 🚦 Campo adicional de **prioridade** (feature implementada durante a mudança de escopo);  
- 🔍 Filtragem e manipulação de tarefas em linha de comando (CLI);  
- 🧪 Testes automatizados com **PyTest** para validação do sistema;  
- 🔄 Execução automática de testes com **GitHub Actions** a cada push.

---

## 🧩 Metodologia e Mudança de Escopo

Durante o desenvolvimento, foi utilizada a metodologia **Kanban**, organizada no GitHub Projects, com as colunas:

- **To Do (A Fazer)**  
- **In Progress (Em Progresso)**  
- **Done (Concluído)**  

Cada card representou uma etapa ou tarefa do projeto, acompanhando o progresso ao longo do ciclo de desenvolvimento.

Durante o processo, foi realizada uma **mudança de escopo planejada**, que incluiu o acréscimo do campo **“prioridade”** nas tarefas — representando a adaptação a novas demandas dentro de um ambiente ágil.

---

## ⚙️ Estrutura do Projeto


AgilTaskFlow/

├── .github/
│   └── workflows/
│       └── python-app.yml    # CI/CD configurado com PyTest
|
├── data/
│   └── tasks.json            # Base de dados local (JSON)
|
├── docs/
│   ├── theory.md             # Parte teórica, conceitos e diagramas UML
│   ├── video_pitch_script.md # Roteiro para o vídeo pitch do projeto
│   └── prints/               # Evidências (prints de Kanban, workflows, etc.)
|
├── src/
│   ├── app.py                # Arquivo principal do sistema
│   └── tasks.py              # Lógica de manipulação das tarefas (CRUD)
|
├── tests/
│   ├── test_app.py           # Testes unitários do app principal
│   ├── test_tasks.py         # Testes unitários das funções principais
│   └── test_tasks_extra.py   # Testes unitários complementares
|
├── pytest.ini                # Arquivo de configuração do PyTest
├── requirements.txt          # Dependências do projeto
└── README.md                 # Onde você está agora! (Visão geral do projeto)


---

## 🧪 Testes Automatizados e Integração Contínua

Os testes foram implementados com **PyTest**, garantindo a confiabilidade das operações CRUD.

A integração contínua (**CI**) foi configurada via **GitHub Actions**, executando automaticamente os testes a cada novo *commit*.

- Executar testes localmente:

  ```bash
  pytest -q

  Resultado esperado:

  ...                                                                 [100%]
3 passed in 0.20s

O status do pipeline pode ser visualizado na aba Actions do repositório GitHub, com os testes passando automaticamente (Com os Workflows Runs na cor: ✅ Verde).

---

## 📊 Prints e Evidências

As evidências do projeto estão localizadas na pasta **/docs/prints**, incluindo:

- Print do Kanban (GitHub Projects);
- Print do workflow Actions bem-sucedido;
- Prints de execução de testes locais e estrutura final.

✅ Essas imagens comprovam o funcionamento completo do ciclo ágil e o cumprimento de todos os requisitos.

---

## 🎥 Vídeo Pitch

Um vídeo de apresentação (pitch) foi gravado com duração aproximada de 3 a 4 minutos, demonstrando:

- O funcionamento do sistema (CRUD);
- A aplicação das metodologias ágeis;
- A execução dos testes e o pipeline do GitHub Actions;
- A mudança de escopo e a conclusão do projeto.

📎 Link do vídeo: (adicionar aqui o link do YouTube ou Google Drive quando disponível)

---

## 💡 Tecnologias Utilizadas

- Python 3.13
- PyTest
- Git & GitHub
- GitHub Actions (CI/CD)
- Kanban (GitHub Projects)
- JSON (armazenamento local)

---

## 👨‍💻 Autor

---

**Lucas Ferreira da Silva**

**Projeto desenvolvido como parte da disciplina de Software Engineering - EAD**

**Trabalho referente ao 3º Semestre do curso de Engenharia da Computação — UniFECAF**

**© 2025 — Todos os direitos reservados.**

---

## 🏁 Status Final

✅ Ambiente configurado

✅ Estrutura de pastas concluída

✅ Testes automatizados aprovados

✅ CI/CD funcional (Actions)

✅ Documentação teórica e roteiro do vídeo incluídos

✅ Prints e evidências anexadas

✅ Projeto pronto para entrega e avaliação final

---