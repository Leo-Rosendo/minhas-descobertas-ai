Copie e cole este conteúdo no arquivo `.md` do GitHub:

````markdown
# 🔍 Guide: Find-Skills (A Meta-Skill)

> O guia definitivo para o Claude encontrar e instalar outras skills para você.  
> **Por:** Leo Rosendo | **Baseado em:** Registry público do Vercel Labs

---

## 🧠 O que é isso?

A **find-skills** não é uma ferramenta que faz o trabalho sozinha. Ela é uma **instrução** que ensina o Claude a usar o terminal para buscar, no repositório oficial `skills.sh`, as melhores ferramentas para o que você precisa.

**Resumo:** em vez de você caçar skills no Google, o Claude faz a pesquisa e a instalação para você.

---

## ✅ Pré-requisitos

Antes de começar, certifique-se de ter:

| Requisito | Como verificar | Link |
|---|---|---|
| **Node.js 18+** | `node -v` e `npm -v` | [Baixar Node.js](https://nodejs.org/) |
| **Claude Code configurado** | `claude --version` | [Claude Code Docs](https://docs.claude.com/) |
| **Terminal com permissões** | Conseguir rodar `npx` | — |

> ⚠️ **Importante:** se não tiver o Node.js instalado, a instalação da skill não funcionará.

---

## 🚀 Instalação

Abra o terminal no seu projeto, ou no Claude Code, e rode este comando:

### 🍎 Mac/Linux

```bash
npx skills add https://github.com/vercel-labs/skills --skill find-skills
```

### 🪟 Windows, ou se travar

```bash
npx -y skills add https://github.com/vercel-labs/skills --skill find-skills --yes
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
npx skills add <id-da-skill> -y
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
| 🧪 Teste antes de usar em produção | Instale a skill em um projeto de teste primeiro para validar o comportamento. |

---

## 🔗 Links Úteis

- 🌐 [Registry Oficial de Skills](https://skills.sh)
- 📚 [Documentação do CLI no GitHub](https://github.com/vercel-labs/skills)
- 💬 [Comunidade Claude Code (Discord)](https://discord.gg/anthropic)
- 📖 [Guia oficial do Claude Code](https://docs.claude.com/)

---

## ⚠️ Problemas Comuns

| Problema | Solução |
|---|---|
| `Error: Unknown skill: find-skills` | A skill não é chamada diretamente. Descreva o que quer encontrar e o Claude usa a skill automaticamente. |
| Comando trava no terminal | Use `npx -y ... --yes` para pular confirmações interativas. |
| `npm warn exec The following package was not found...` | Normal na primeira vez. O `npx` está baixando o pacote `skills`. Aguarde. |
| Claude não está usando a skill | Reinicie o Claude Code e rode `/skills` para confirmar que ela aparece como `on`. |
| Busca não retorna resultados | Peça para tentar outras palavras-chave ou ser mais específico. |
| `Permission denied` no terminal | No Mac/Linux, tente `sudo npx ...` ou ajuste as permissões da pasta. |
| Skill some ao mudar de projeto | Skills em `.agents/skills/` são locais do projeto. Use `--global` para instalar em todos. |

---

## 📁 Estrutura de pastas após instalação

```text
seu-projeto/
├── .agents/
│   └── skills/
│       └── find-skills/      ← skill instalada aqui
├── .claude/
│   └── skills/
│       └── find-skills       ← symlink para .agents/skills/find-skills
└── ...
```

---

## 🎯 Para quem é essa skill?

| Perfil | Por que usar |
|---|---|
| 👨‍💻 Devs que usam Claude Code diariamente | Descoberta contínua de skills especializadas conforme novas necessidades surgem. |
| 📝 Criadores de conteúdo / SEO | O registry tem uma família robusta de skills de SEO, facilitando montar um kit SEO customizado. |
| ⚡ Profissionais de produtividade | Skills de compactação de contexto e otimização de tokens ajudam em projetos longos. |
| 👥 Equipes técnicas | Padroniza o onboarding: todo mundo instala `find-skills` primeiro e depois descobre as skills do workflow do time. |
| 🆕 Iniciantes em Claude Code | É uma boa skill para começar. Em vez de decorar skills, você aprende a descobri-las sob demanda. |

---

## 🔧 Comandos úteis de referência rápida

```bash
# Instalar find-skills
npx skills add https://github.com/vercel-labs/skills --skill find-skills

# Buscar skills manualmente, sem passar pelo Claude
npx -y skills find "<termo>"

# Instalar qualquer skill encontrada
npx skills add <id-da-skill> -y

# Listar tudo que está instalado
npx skills list

# Atualizar todas as skills
npx skills update

# Ver ajuda completa do CLI
npx skills --help

# Remover uma skill
npx skills remove find-skills
```

---

<div align="center">

<a href="./README.md">⬅️ Voltar para Claude Code Skills</a> |
<a href="../README.md">🏠 Voltar para Home</a>

</div>
````
