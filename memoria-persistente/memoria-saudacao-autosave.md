# 🧠 Memória Persistente para AIOS/AIOX
**Por:** Leo Rosendo  
**Repositório:** github.com/Leo-Rosendo/aios-aiox-templates  
**Versão:** 1.0 | Gratuito

---

⚠️ INFORMAÇÃO IMPORTANTE ANTES DE COMEÇAR

O AIOX tem um sistema de memória nativo, mas só está disponível na versão 
paga (Pro). O que vamos configurar agora é GRATUITO, personalizado e mais 
poderoso — feito sob medida para o seu projeto.

Você só precisa colar o comando abaixo para o agente Orion. Ele faz tudo 
automaticamente. Não precisa mexer em nada — exceto nos campos marcados!

---

📖 LEGENDA — LEIA ANTES DE USAR:

[ ]   → O AGENTE preenche automaticamente. Não mexa!
(( )) → VOCÊ precisa preencher com a sua informação antes de colar.

---

🔒 REGRAS DE SEGURANÇA — O AGENTE DEVE SEGUIR SEMPRE:
- NUNCA salvar senhas, tokens ou API keys nos arquivos de contexto
- SEMPRE usar variáveis de ambiente para dados sensíveis
- NUNCA expor informações pessoais em arquivos compartilhados
- Se encontrar dados sensíveis, alertar o usuário imediatamente

---

## COMANDO — cole isso para o agente Orion:

Orion, configure agora o sistema completo de memória persistente.
Você vai identificar automaticamente os caminhos e criar tudo sozinho.
Siga os passos abaixo:

PASSO 1 — CRIAR ARQUIVO DE CONTEXTO DO PROJETO:
Identifique a pasta raiz do projeto atual e crie o arquivo:
[pasta-do-projeto]/memory/contexto-[nome-do-projeto].md

Exemplo: se o projeto se chama "minha-loja", o arquivo será:
/home/usuario/minha-loja/memory/contexto-minha-loja.md

O arquivo deve conter sempre:
- Data e hora da última atualização
- O que está rodando e funcionando
- O que está pendente e bloqueado
- Quais agentes foram acionados e status de cada um
- O que depende de ação do usuário
- Próximos passos em ordem de prioridade
- Métricas do projeto (identificar automaticamente as mais relevantes
  com base nas conversas)
- ⚠️ NUNCA salvar senhas ou tokens neste arquivo

PASSO 2 — SAUDAÇÃO PERSONALIZADA:
Atualize o arquivo do agente master para que toda ativação inicie assim:

"Fala (( escreva seu nome aqui, ex: Léo ))!
Aqui é o Orion, orquestrando o sistema 🎯

💳 Uso Claude hoje: [ex: 45% do limite diário usado]
💳 Uso Claude semana: [ex: 60% do limite semanal usado]
🐳 Serviços ativos: [ex: 5 containers rodando ✅]
🕐 [data e hora atual]
📊 Métricas: [métricas mais importantes identificadas no contexto]

Aqui está o que ficou da nossa última conversa:
[resumo do contexto — pendentes, o que está rodando,
o que depende do usuário]

Baseado na situação atual, recomendo agora:
[top 1 ação concreta para gerar resultado]

O que você acha?"

PASSO 3 — AUTO-SAVE TOTALMENTE AUTOMÁTICO:
⚠️ O usuário não precisa fazer nada. Você (Orion) configura tudo
para salvar sozinho, mesmo que a pessoa esqueça ou feche o terminal.

Configure automaticamente:
a) Cron a cada 29 minutos:
   */29 * * * * [caminho-identificado-por-você]/scripts/auto-save.sh

b) Auto-save por inatividade de 10 minutos via PROMPT_COMMAND
   no ~/.bashrc

Após configurar tudo, me mostre:
1. crontab -l (para confirmar o auto-save)
2. Confirmação dos 3 passos concluídos
3. Se precisar de alguma informação minha para continuar
