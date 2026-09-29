<%*
const caminho = tp.file.path(true)
const partes = caminho.split("/")

// Remove a extensão .md do nome do arquivo
const nomeArquivo = tp.file.title

// Remove a numeração inicial.
// Exemplo: "01 - Ortografia oficial" → "Ortografia oficial"
const limparNome = (nome) => {
    return nome.replace(/^\d+\s*-\s*/, "").trim()
}

let area = ""
let disciplina = ""
let assunto = ""
let tema = ""

// Estrutura:
// AREA / DISCIPLINA / ARQUIVO.md
if (partes.length === 3) {
    area = limparNome(partes[0])
    disciplina = limparNome(partes[1])
    assunto = limparNome(nomeArquivo)
}

// Estrutura:
// AREA / DISCIPLINA / ASSUNTO / ARQUIVO.md
else if (partes.length >= 4) {
    area = limparNome(partes[0])
    disciplina = limparNome(partes[1])
    assunto = limparNome(partes[partes.length - 2])
    tema = limparNome(nomeArquivo)
}

const statusOptions = [
    "Não iniciado",
    "Estudando",
    "Revisão",
    "Concluído"
]

const dificuldadeOptions = [
    "Fácil",
    "Média",
    "Difícil"
]

const status = await tp.system.suggester(
    statusOptions,
    statusOptions
)

const dificuldade = await tp.system.suggester(
    dificuldadeOptions,
    dificuldadeOptions
)

const hoje = tp.date.now("YYYY-MM-DD")
%>
---
area: "<% area %>"
disciplina: "<% disciplina %>"
assunto: "<% assunto %>"
tema: "<% tema %>"
status: "<% status %>"
dificuldade: "<% dificuldade %>"
questoes: 0
acertos: 0
erros: 0
revisoes: 0
ultima_revisao:
proxima_revisao:
criado_em: <% hoje %>
---
> 📚 [[INDICE|Índice geral]]  
> 📖 **Área:** <% area %>  
> 📘 **Disciplina:** <% disciplina %>  
> 📑 **Assunto:** <% assunto %><% tema ? `  \n> 📝 **Tema:** ${tema}` : "" %>

---

## 📑 Sumário

- [[#Resumo]]
- [[#Conceitos]]
- [[#Exemplos]]
- [[#Pegadinhas]]
- [[#Questões]]
- [[#Erros]]
- [[#Revisão]]

---

## 📝 Resumo

> Escreva aqui um resumo objetivo do assunto.

---

## 📚 Conceitos

### Conceito principal



### Pontos importantes

- 
- 
- 

---

## 💡 Exemplos



---

## ⚠️ Pegadinhas

> Pontos que podem induzir ao erro em provas.

- 
- 
- 

---

## 📝 Questões

### Questões resolvidas

| Questão | Resultado | Observação |
|---|---|---|
|  |  |  |

### Desempenho

- **Questões:** 0
- **Acertos:** 0
- **Erros:** 0
- **Percentual:** 0%

---

## ❌ Erros

> Registre aqui os erros cometidos durante os exercícios.

### Erro 01



### Como evitar



---

## 🔄 Revisão

**Última revisão:**  
**Próxima revisão:**  

### Pontos para revisar

- [ ] 
- [ ] 
- [ ] 

---

> [!tip] Método de estudo
> **Teoria → Exemplos → Questões → Erros → Revisão**

---

⬅️ [[INDICE|Voltar ao índice]]