# SetupKit Clarify

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licença: **MIT**

[English](README.md) · [Español](README.es.md) · Português (Brasil) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Transforme um pedido pouco claro em um briefing que permita avançar.

## Quando usar

Use o Clarify quando uma pergunta sem resposta puder mudar o escopo, o custo, o risco ou a definição de sucesso. Ele aproveita o contexto disponível, pergunta apenas sobre lacunas relevantes e para quando há informação suficiente para continuar.

O resultado registra o escopo definido, as premissas aceitas, as perguntas adiadas e o próximo passo.

## Instalação

Leia primeiro as instruções do skill. Para a primeira tentativa, use um projeto de teste novo e vazio. Antes de executar o comando, verifique se já existem pastas do skill nos destinos e locais compartilhados do projeto; decida qualquer atualização separadamente. Consulte o [guia geral de instalação](../../INSTALL.pt.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Escolha o assistente de destino e o escopo do projeto. Revise as opções pré-selecionadas, os destinos e o resumo final antes de confirmar. Alguns assistentes compartilham .agents/skills; outros assistentes do projeto podem descobrir os arquivos colocados ali.

npx baixa e executa o instalador. O guia comum de instalação informa as versões e os modos testados e os limites de compatibilidade.

## Exemplos

Ilustrações, não registros de execuções reais. As perguntas só se aplicam quando as respostas não estão no contexto.

### Automatizar um relatório semanal

**Pedido de exemplo:**

```text
Use setupkit-clarify: gasto tempo demais no nosso relatório semanal. Ajude-me a decidir o que automatizar.
```

**Possíveis perguntas:**

- De onde vêm os dados do relatório?
- Quem usa o relatório e que decisão ele deve ajudar essa pessoa a tomar?
- Quais etapas podem rodar automaticamente e quais precisam da sua revisão?

**Resultado ilustrativo:** Um fluxo com limites definidos: entradas, resultado útil, etapas automáticas e pontos de revisão humana. Este briefing não autoriza a implementação nem o envio do relatório.

### Definir um post de lançamento

**Pedido de exemplo:**

```text
Use setupkit-clarify: quero anunciar o lançamento do nosso produto. Ajude-me a definir o post antes de escrevê-lo.
```

**Possíveis perguntas:**

- Quem deve ler o post e o que deve entender?
- Qual é a ideia principal que você quer transmitir?
- Quais resultados ou afirmações sobre o produto podemos comprovar e que resposta você espera?

**Resultado ilustrativo:** Um briefing de conteúdo com o leitor, a ideia do autor, as afirmações respaldadas e a resposta desejada.

## Limites

As perguntas dos exemplos são ilustrativas. O Clarify não impõe um questionário fixo nem pede novamente respostas já disponíveis. Um pedido simples e bem definido pode avançar sem mais perguntas.

Os skills continuam sujeitos às permissões e regras de aprovação do seu assistente. Eles não concedem acesso a contas nem autorizam gastos, envios, instalações ou publicações.

Compartilhe com o assistente escolhido apenas material que você tenha o direito de compartilhar. Confira as condições de tratamento de dados antes de fornecer informações confidenciais ou pessoais.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.pt.md)

## Licença e procedência

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Desenvolvidos com assistência do OpenAI Codex.

Consulte a [procedência](../PROVENANCE.md) para conhecer o histórico de desenvolvimento e os trabalhos relacionados conhecidos. O crédito de autoria cobre estas implementações mantidas; não reivindica a invenção dos métodos gerais de perguntas ou checagem de fatos.

O nome do autor, o link para o SetupKit, o identificador MIT e o texto completo da licença também permanecem em cada SKILL.md, acompanhando uma cópia independente.

O inglês é a fonte de referência. As traduções dos README descrevem os mesmos skills; cada skill tem um único SKILL.md em inglês.
