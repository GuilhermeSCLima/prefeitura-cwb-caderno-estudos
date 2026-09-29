# 📚 Caderno de Estudos

> Índice e painel de acompanhamento dos estudos.

---

# 📊 Progresso

## 📚 Total de temas

```dataview
TABLE WITHOUT ID
    length(rows) AS "Total de temas"
FROM ""
WHERE file.name != "INDICE"
GROUP BY true
```

## 📌 Temas por status

```dataview
TABLE WITHOUT ID
    status AS "Status",
    length(rows) AS "Quantidade"
FROM ""
WHERE status
GROUP BY status
SORT status ASC
```

## 🎯 Temas por dificuldade

```dataview
TABLE WITHOUT ID
    dificuldade AS "Dificuldade",
    length(rows) AS "Quantidade"
FROM ""
WHERE dificuldade
GROUP BY dificuldade
SORT dificuldade ASC
```

---

# 📅 Revisões

## 🔔 Revisões pendentes

```dataview
TABLE
    area AS "Área",
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    proxima_revisao AS "Próxima revisão"
FROM ""
WHERE proxima_revisao
AND proxima_revisao <= date(today)
SORT proxima_revisao ASC
```

---

# 📚 Conhecimentos Básicos

## 📖 Conteúdo

```dataview
TABLE
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    status AS "Status",
    dificuldade AS "Dificuldade"
FROM "Conhecimentos Básicos"
WHERE disciplina
SORT disciplina ASC, assunto ASC, tema ASC
```

---

# 📘 Conhecimentos Específicos

## 📖 Conteúdo

```dataview
TABLE
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    status AS "Status",
    dificuldade AS "Dificuldade"
FROM "Conhecimentos Específicos"
WHERE disciplina
SORT disciplina ASC, assunto ASC, tema ASC
```

---

# 📝 Assuntos não iniciados

```dataview
TABLE
    area AS "Área",
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    dificuldade AS "Dificuldade"
FROM ""
WHERE status = "Não iniciado"
SORT area ASC, disciplina ASC, assunto ASC, tema ASC
```

---

# 📖 Em estudo

```dataview
TABLE
    area AS "Área",
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    dificuldade AS "Dificuldade"
FROM ""
WHERE status = "Estudando"
SORT area ASC, disciplina ASC, assunto ASC, tema ASC
```

---

# 🔄 Em revisão

```dataview
TABLE
    area AS "Área",
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    dificuldade AS "Dificuldade",
    proxima_revisao AS "Próxima revisão"
FROM ""
WHERE status = "Revisão"
SORT proxima_revisao ASC
```

---

# ✅ Concluídos

```dataview
TABLE
    area AS "Área",
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    questoes AS "Questões",
    acertos AS "Acertos",
    erros AS "Erros"
FROM ""
WHERE status = "Concluído"
SORT area ASC, disciplina ASC, assunto ASC, tema ASC
```

---

# ❌ Questões com erros

```dataview
TABLE
    area AS "Área",
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    questoes AS "Questões",
    acertos AS "Acertos",
    erros AS "Erros"
FROM ""
WHERE erros > 0
SORT erros DESC
```

---

# 📈 Desempenho

```dataview
TABLE
    area AS "Área",
    disciplina AS "Disciplina",
    assunto AS "Assunto",
    tema AS "Tema",
    questoes AS "Questões",
    acertos AS "Acertos",
    erros AS "Erros"
FROM ""
WHERE questoes > 0
SORT erros DESC
```

---

# 🎯 Método de estudo

```text
┌─────────────┐
│    Teoria   │
└──────┬──────┘
       ↓
┌─────────────┐
│  Exemplos   │
└──────┬──────┘
       ↓
┌─────────────┐
│   Questões  │
└──────┬──────┘
       ↓
┌─────────────┐
│    Erros    │
└──────┬──────┘
       ↓
┌─────────────┐
│   Revisão   │
└─────────────┘
```

> **Estudar → Praticar → Identificar erros → Revisar → Repetir**

---

# 🗂️ Estrutura do caderno

```text
Caderno
│
├── Conhecimentos Básicos
│   ├── 1.1 Língua Portuguesa
│   ├── 1.2 Raciocínio Lógico
│   ├── 1.3 Noções de Informática
│   └── 1.4 Legislação
│
├── Conhecimentos Específicos
│   ├── 2.1 Fundamentos da Administração Pública
│   ├── 2.2 Direito Administrativo
│   ├── 2.3 Direito Constitucional
│   ├── 2.4 Ética, Relacionamento e Atendimento no Serviço Público
│   ├── 2.5 Gestão da Informação, Arquivologia e Redação Oficial
│   └── 2.6 Métodos e Técnicas de Pesquisa
│
├── _templates
│   └── Assunto.md
│
└── INDICE.md
```

---

# 🛠️ Ferramentas

- 📚 **Obsidian** — organização do caderno
    
- 📊 **Dataview** — consultas e indicadores
    
- ⚙️ **Templater** — geração das notas
    
- 🌱 **Obsidian Git** — versionamento