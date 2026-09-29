# 📚 Caderno de Estudos — Concurso Público

> Caderno de estudos desenvolvido em [Obsidian](https://obsidian.md/) para organização, acompanhamento e revisão do conteúdo programático de concurso público.

Este repositório contém meu caderno de estudos estruturado em Markdown, utilizando propriedades, templates e consultas Dataview para organizar o conteúdo e acompanhar a evolução dos estudos.

O conteúdo é gerado e organizado a partir de uma estrutura hierárquica de áreas, disciplinas, assuntos e temas.

---

## 🎯 Objetivo

Centralizar e organizar a preparação para o concurso em uma estrutura que facilite:

- 📚 estudo da teoria;
    
- 📝 criação de resumos;
    
- 💡 registro de exemplos;
    
- ⚠️ identificação de pegadinhas;
    
- 📝 resolução de questões;
    
- ❌ registro de erros;
    
- 🔄 revisões periódicas;
    
- 📊 acompanhamento do progresso.
    

A proposta é transformar o caderno em uma base de estudos estruturada, permitindo acompanhar não apenas o conteúdo estudado, mas também o desempenho ao longo da preparação.

---

## 🗂️ Estrutura

O conteúdo segue uma estrutura hierárquica:

```text
Área
└── Disciplina
    ├── Assunto.md
    └── Assunto
        ├── Tema.md
        └── Tema.md
```

Quando um assunto possui subdivisões, ele é representado como uma pasta contendo seus respectivos temas.

Exemplo:

```text
Conhecimentos Básicos
└── 1.1 Língua Portuguesa
    ├── 1.1.10 Pontuação.md
    ├── 1.1.11 Uso dos porquês.md
    └── 1.1.1 Análise e interpretação de texto
        ├── 1.1.1.1 compreensão global.md
        ├── 1.1.1.2 ponto de vista do autor.md
        ├── 1.1.1.3 ideias centrais desenvolvidas em cada parágrafo.md
        └── 1.1.1.4 inferências.md
```

A numeração segue a organização do conteúdo programático utilizado como base para o caderno.

---

## 📖 Conteúdo

### Conhecimentos Básicos

- Língua Portuguesa
    
- Raciocínio Lógico
    
- Noções de Informática
    
- Legislação
    

### Conhecimentos Específicos

- Fundamentos da Administração Pública
    
- Direito Administrativo
    
- Direito Constitucional
    
- Ética, Relacionamento e Atendimento no Serviço Público
    
- Gestão da Informação, Arquivologia e Redação Oficial
    

O conteúdo completo está disponível no:

[`INDICE.md`](https://chatgpt.com/c/INDICE.md)

---

## 📊 Acompanhamento dos estudos

Cada nota possui propriedades estruturadas no frontmatter:

```yaml
---
area:
disciplina:
assunto:
tema:
status: "Não iniciado"
dificuldade: "Fácil"
questoes: 0
acertos: 0
erros: 0
revisoes: 0
ultima_revisao:
proxima_revisao:
criado_em:
---
```

Essas propriedades permitem utilizar o **Dataview** para gerar automaticamente indicadores como:

- quantidade de assuntos;
    
- quantidade de temas;
    
- progresso por disciplina;
    
- progresso por área;
    
- assuntos não iniciados;
    
- assuntos em estudo;
    
- assuntos em revisão;
    
- assuntos concluídos;
    
- distribuição por dificuldade;
    
- quantidade de questões;
    
- quantidade de acertos;
    
- quantidade de erros;
    
- percentual de aproveitamento;
    
- revisões pendentes.
    

---

## 📝 Estrutura das notas

As notas são padronizadas através de um template.

Cada tema possui uma estrutura semelhante a:

```text
📚 Assunto

├── 📝 Resumo
├── 📚 Conceitos
├── 💡 Exemplos
├── ⚠️ Pegadinhas
├── 📝 Questões
├── ❌ Erros
└── 🔄 Revisão
```

O template utilizado atualmente está localizado em:

```text
_templates/
└── Assunto.md
```

O **Templater** é responsável por gerar a estrutura inicial da nota e preencher automaticamente informações como:

- área;
    
- disciplina;
    
- assunto;
    
- tema;
    
- data de criação;
    
- status;
    
- dificuldade.
    

---

## 🧰 Ferramentas

|Ferramenta|Finalidade|
|---|---|
|[Obsidian](https://obsidian.md/)|Organização das notas|
|[Dataview](https://github.com/blacksmithgu/obsidian-dataview)|Consultas e indicadores|
|[Templater](https://github.com/SilentVoid13/Templater)|Templates e automações|
|Obsidian Git|Versionamento do vault|
|Markdown|Formato das notas|
|Git|Controle de versão|

---

## 📑 Índice

O `INDICE.md` funciona como a página principal do caderno.

Ele centraliza:

```text
INDICE.md
│
├── 📊 Progresso
├── 📅 Revisões
├── 📚 Conhecimentos Básicos
├── 📘 Conhecimentos Específicos
├── 📝 Assuntos não iniciados
├── 📖 Assuntos em estudo
├── 🔄 Assuntos em revisão
├── ✅ Assuntos concluídos
└── ❌ Questões com erros
```

As informações de acompanhamento são obtidas automaticamente através das propriedades das notas e das consultas Dataview.

---

## 🔄 Fluxo de estudo

O método utilizado no caderno segue o ciclo:

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

**Estudar → Praticar → Identificar erros → Revisar → Repetir**

---

## 🛠️ Gerador de cadernos

A estrutura do caderno pode ser criada automaticamente através do projeto de geração de estruturas.

O gerador é responsável por transformar uma estrutura de dados em:

- diretórios;
    
- disciplinas;
    
- assuntos;
    
- temas;
    
- arquivos Markdown.
    

Isso permite reproduzir rapidamente a estrutura do conteúdo programático sem precisar criar manualmente centenas de pastas e arquivos.

---

## 🌱 Versionamento

O caderno utiliza Git para acompanhar sua evolução.

Os commits seguem uma estrutura inspirada em [Conventional Commits](https://www.conventionalcommits.org/):

```text
tipo(escopo): descrição
```

Exemplos:

```text
docs(portugues): adiciona pontuação

docs(raciocinio-logico): adiciona probabilidade

template(assunto): atualiza estrutura das notas

feat(indice): adiciona painel de progresso

fix(templater): corrige identificação do assunto
```

O versionamento permite acompanhar tanto a evolução do conteúdo quanto as alterações realizadas na estrutura do caderno.

---

## 🚀 Utilização

### Requisitos

- [Obsidian](https://obsidian.md/)
    
- Git
    

### Clonar o repositório

```bash
git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
```

Depois, abra a pasta clonada no Obsidian utilizando:

```text
Open folder as vault
```

Os plugins utilizados pelo vault ficam registrados na configuração do Obsidian.

---

## ⚠️ Observações

Este repositório representa um caderno pessoal de estudos.

O conteúdo pode conter:

- resumos;
    
- anotações;
    
- exemplos;
    
- questões;
    
- referências;
    
- materiais produzidos durante a preparação.
    

Materiais de terceiros protegidos por direitos autorais não devem ser adicionados ao repositório sem autorização.

Para informações oficiais sobre o concurso, edital, alterações ou comunicados, consulte sempre as fontes oficiais do órgão responsável e da organizadora do certame.

---

## 📄 Licença

Este repositório contém material de estudo pessoal.

A licença do conteúdo será definida posteriormente.