# Instalar os skills do SetupKit

[English](INSTALL.md) · [Español](INSTALL.es.md) · Português (Brasil) · [日本語](INSTALL.ja.md) · [Deutsch](INSTALL.de.md) · [Français](INSTALL.fr.md) · [Русский](INSTALL.ru.md) · [简体中文](INSTALL.zh.md)

Escolha [Clarify](skills/setupkit-clarify/README.pt.md) para transformar um pedido vago em um briefing, ou [Fact Check](skills/setupkit-fact-check/README.pt.md) para revisar afirmações e evidências. Leia o SKILL.md escolhido antes de instalar.

Este guia trata da instalação em um projeto. Para a primeira experiência, use um projeto de teste novo e vazio. Estas instruções não conectam contas nem exigem chave ou API de modelos paga. Continuam valendo os custos e as permissões do seu assistente.

## Antes de instalar

1. Escolha um ou ambos os skills e o assistente que vai usar.
2. Confira as pastas de destino do assistente e as compartilhadas `.agents/skills/setupkit-clarify` e `.agents/skills/setupkit-fact-check`. Se alguma já existir, pare e decida essa atualização separadamente. Os avisos de sobrescrita podem não cobrir todos os destinos compartilhados.
3. Escolha o escopo do projeto. Vários assistentes usam `.agents/skills`; outros assistentes do mesmo projeto podem descobrir esses arquivos.

## Skills CLI

A [documentação original do Skills CLI](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md) inclui Codex, Claude Code, Cursor, Gemini CLI, OpenCode, Windsurf e GitHub Copilot. O manifesto do repositório inspecionado exige Node.js 22.20.0 ou posterior. Use o ambiente exigido pela versão escolhida.

Abra um terminal na pasta do projeto de destino. `npx` baixa e executa o instalador; revise o pacote original antes de executá-lo.

Ambos os skills:

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Apenas Clarify:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Apenas Fact Check:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Escolha o assistente e o escopo do projeto. Confira todas as opções pré-selecionadas, os caminhos e o resumo final antes de confirmar. Cancele se um skill existente seria substituído sem uma atualização acordada separadamente. Estes exemplos mantêm a confirmação ativada.

Para indicar um destino, acrescente seu identificador, como `--agent cursor`, `--agent gemini-cli` ou `--agent opencode`. A [tabela original de destinos](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md#supported-agents) lista outros identificadores e diretórios.

Destinos representativos do código inspecionado:

| Destino do instalador | Diretório do projeto |
|---|---|
| Codex, Cursor, Gemini CLI, OpenCode, GitHub Copilot | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Windsurf | `.windsurf/skills/` |

Esta tabela descreve o roteamento do instalador; não comprova que o SetupKit foi testado em cada assistente. Os comandos acima não fixam uma versão: uma versão posterior pode diferir do código inspecionado.

## Alternativa para Codex

Se skill-installer estiver disponível no seu ambiente Codex, abra o projeto de destino e envie:

```text
$skill-installer Instale SetupKit Clarify e SetupKit Fact Check a partir de:
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-clarify
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-fact-check
Instale somente neste projeto. Preserve os skills existentes. Se a instalação no projeto não estiver disponível, explique a limitação sem alterar arquivos.
```

Para um único skill, inclua apenas o nome e a URL dele. O pedido expressa o escopo desejado; confirme o destino real antes de permitir mudanças. Se só houver instalação para todo o usuário, pare e escolha um método para o projeto. Consulte a [orientação oficial do Codex](https://learn.chatgpt.com/docs/build-skills).

## Instalação manual e Claude Code

Baixe o arquivo do repositório no GitHub e extraia fora das pastas em que o assistente descobre skills. Leia os SKILL.md selecionados. Copie apenas as pastas escolhidas de `skills/` para o diretório do projeto documentado pelo assistente, mantendo nomes e conteúdo. Confira os destinos específicos e compartilhados; não substitua uma pasta sem uma decisão separada de atualização.

Codex, escopo do projeto:

```text
.agents/skills/setupkit-clarify/SKILL.md
.agents/skills/setupkit-fact-check/SKILL.md
```

Claude Code, escopo do projeto:

```text
.claude/skills/setupkit-clarify/SKILL.md
.claude/skills/setupkit-fact-check/SKILL.md
```

Para instalar só um skill, basta sua pasta. Preserve as traduções de README que copiar e todos os avisos de autoria e licença em SKILL.md. No Claude Code, depois da descoberta, comece a mensagem com `/setupkit-clarify` ou `/setupkit-fact-check`. Consulte a [documentação oficial do Claude Code](https://code.claude.com/docs/en/skills).

Em outro assistente, verifique o caminho oficial de descoberta e o método de invocação. Mantenha uma cópia das instruções de cada skill; adaptar um caminho não exige traduzir nem reescrever SKILL.md.

## Confira o resultado

1. Confirme que os identificadores escolhidos aparecem na lista ou visualização de descoberta do assistente com escopo do projeto. Inicie uma nova tarefa ou reinicie o assistente se necessário.
2. Experimente um exemplo de [Clarify](skills/setupkit-clarify/README.pt.md) ou [Fact Check](skills/setupkit-fact-check/README.pt.md). Confira se o skill correto foi realmente carregado.
3. Compare o resultado com o objetivo do exemplo. Clarify deve perguntar só por informações relevantes que faltam. Fact Check deve mostrar lacunas nas evidências e uma decisão apropriada, incluindo BLOCK quando necessário.

## Compatibilidade e permissões

A estrutura de arquivos e os padrões de comandos foram comparados com documentação e código original capturados. O escopo dos testes com versões específicas está abaixo; esses testes não fornecem evidência de invocação nativa nos outros assistentes listados. Um destino do instalador não comprova igualdade de ativação, ferramentas, acesso a fontes, permissões ou qualidade da revisão.

Fact Check precisa de acesso a fontes atuais para afirmações que mudam com o tempo. Se faltarem evidências relevantes, a afirmação continua sem resolução. O pacote não inclui nem instala um humanizer; Fact Check pode funcionar sem ele.

O assistente controla carregamento, execução e permissões. Um skill ou uma decisão PASS não autoriza publicar, enviar, gastar, instalar ou conectar contas. Compartilhe apenas materiais que você tem direito de fornecer ao assistente e revise os termos de tratamento de dados dele.

## Modo de teste verificado

Em 18 de outubro de 2026, a instalação por cópia em projetos macOS novos foi verificada com npm/npx 11.6.2 e Skills CLI 1.7.2. Ambos os skills foram invocados explicitamente no Codex 0.163.0-alpha.10.2 (gpt-6.1-sol) e no OpenCode 2.0.22 (gpt-5.6-sol), usando uma assinatura existente do ChatGPT. Os testes sintéticos cobriram briefings incompletos/completos e afirmações sem respaldo/corretas.

O ambiente de teste desativou os scripts de ciclo de vida do npm.

Comando testado para copiar no Codex sem interação:

```bash
npx --yes skills@1.7.2 add etsarkov/setupkit-ai --skill setupkit-clarify --skill setupkit-fact-check --agent codex --copy --yes --json
```

Para o destino OpenCode testado, substitua `codex` por `opencode`. Use esse modo sem confirmações apenas depois de conferir por conta própria os skills, o escopo do projeto e todas as pastas de destino. Os exemplos anteriores mantêm a confirmação.

Esses testes não verificam as opções interativas padrão, o modo padrão de links simbólicos, a instalação global, a ativação automática, a checagem de fontes web ao vivo ou outras versões de assistentes. Não garantem a qualidade do resultado em qualquer tarefa.

## Autor e licença

Autor e mantenedor: [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Parte do [SetupKit](https://github.com/etsarkov/setupkit-ai), desenvolvido com ajuda do OpenAI Codex. Estes dois skills usam a [licença MIT](skills/LICENSE); consulte a [procedência](skills/PROVENANCE.md). O guia principal do SetupKit tem licença própria, descrita no [README do repositório](README.md#author-and-reuse).

O inglês é a fonte de referência. Esta tradução mantém as mesmas instruções, identificadores e limites.
