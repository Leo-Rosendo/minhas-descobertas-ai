


# 🔍 Guide: Find-Skills (A Meta-Skill)

> O guia definitivo para o Claude encontrar e instalar outras skills para você.  
> **Por:** Leo Rosendo | **Baseado em:** Registry público do Vercel Labs

---

## 🧠 O que é isso?

A **find-skills** não é uma ferramenta que faz o trabalho sozinha. Ela é uma **instrução** que ensina o Claude a usar o terminal para buscar, no repositório oficial `skills.sh`, as melhores ferramentas para o que você precisa.

**Resumo:** em vez de você caçar skills no Google, o Claude faz a pesquisa e a instalação para você.

---

## 🚀 Instalação

Abra o terminal no seu projeto, ou no Claude Code, e rode este comando:

### 🍎 Mac/Linux

```bash
npx skills add https://github.com/vercel-labs/skills --skill find-skills
```

### 🪟 Windows, ou se travar

```bash
npx -y skills add https://github.com/vercel-labs/skills --skill find-skills
```

> ⚠️ **Dica:** se o terminal travar pedindo confirmação, use as flags `-y` ou `--yes`.

---

## 🗣️ Como usar na prática

Depois de instalar, você não precisa digitar `/find-skills`. Basta conversar com o Claude naturalmente.

Exemplos de prompts que funcionam:

- `Tem alguma skill que ajude a otimizar tokens?`
- `Procure skills para fazer auditoria de SEO.`
- `Quais skills existem para trabalhar com Obsidian?`
- `Tem alguma skill boa para code review?`
- `Liste skills populares para desenvolvimento frontend.`

---

## ⚙️ O que vai acontecer

Quando você pedir algo relacionado a buscar skills, o Claude vai:

1. Rodar comandos no terminal, como:

```bash
npx skills find "termo"
```

2. Buscar por várias palavras-chave relacionadas ao que você pediu.

3. Voltar com uma tabela comparativa das melhores opções.

4. Esperar você escolher a skill desejada.

5. Instalar a skill escolhida com um comando como:

```bash
npx skills add
```

---

## 💡 Dicas de Ouro

| Dica | Por que importa |
|---|---|
| 🔒 Segurança | O instalador roda um scan automático, como Snyk. Se aparecer `Med Risk` ou `High Risk`, pergunte ao Claude o que significa antes de instalar. |
| 🌍 Instalação Global | Se quiser usar a skill em todos os projetos, use `--user` ou `--global` no comando de instalação. |
| 🔄 Atualização | De vez em quando, rode `npx skills update` para garantir que suas ferramentas estão na última versão. |
| 🗑️ Remover | Se der erro ou quiser limpar, use `npx skills remove find-skills`. |
| 🔍 Buscas sem resultado | Peça ao Claude para tentar sinônimos. Em vez de `memória`, tente `context`, `cache` ou `persistence`. |

---

## 🔗 Links Úteis

- [🌐 Registry Oficial de Skills](https://skills.sh)
- [📚 Documentação do CLI no GitHub](https://github.com/vercel-labs/skills)
- [💬 Comunidade Claude Code (Discord)](https://discord.gg/anthropic)

---

## ⚠️ Problemas Comuns

| Problema | Solução |
|---|---|
| `Error: Unknown skill: find-skills` | A skill não é chamada diretamente. Descreva o que quer encontrar e o Claude usa a skill automaticamente. |
| Comando trava no terminal | Use `npx -y ... --yes` para pular confirmações interativas. |
| Claude não está usando a skill | Reinicie o Claude Code e rode `/skills` para confirmar que ela aparece como `on`. |
| Busca não retorna resultados | Peça para tentar outras palavras-chave ou ser mais específico. |

---

<div align="center">

<a href="./README.md">⬅️ Voltar para Claude Code Skills</a> |
<a href="../README.md">🏠 Voltar para Home</a>

</div>
