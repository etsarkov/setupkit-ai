# SetupKit Skills

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licença: **MIT**

[English](README.md) · [Español](README.es.md) · Português (Brasil) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Esclareça a tarefa antes de começar. Revise as evidências antes de publicar.

## Escolha um skill

| Sua situação | Skill | O que você recebe |
|---|---|---|
| Um pedido tem lacunas que podem mudar a tarefa | [Clarify](setupkit-clarify/README.pt.md) | Perguntas objetivas e um escopo mais claro |
| Um texto público ou uma afirmação precisa de revisão factual | [Fact Check](setupkit-fact-check/README.pt.md) | Um registro de afirmações, lacunas de evidência e uma decisão de revisão |

A página de cada skill inclui os cenários de exemplo selecionados e um link para o SKILL.md completo.

## Instalação

Leia primeiro as instruções do skill. Para a primeira tentativa, use um projeto de teste novo e vazio. Antes de executar o comando, verifique se já existem pastas do skill nos destinos e locais compartilhados do projeto; decida qualquer atualização separadamente. Consulte o [guia geral de instalação](../INSTALL.pt.md).

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Escolha o assistente de destino e o escopo do projeto. Revise as opções pré-selecionadas, os destinos e o resumo final antes de confirmar. Alguns assistentes compartilham .agents/skills; outros assistentes do projeto podem descobrir os arquivos colocados ali.

npx baixa e executa o instalador. O guia comum de instalação informa as versões e os modos testados e os limites de compatibilidade.

## Como usar os skills

Depois que o assistente carregar o skill, use o identificador setupkit-clarify ou setupkit-fact-check. Descoberta, acionamento, acesso a fontes e permissões de ferramentas dependem do ambiente; o suporte a um destino no instalador não comprova comportamento idêntico entre assistentes.

O Fact Check pode vir depois de uma etapa editorial, como um humanizer. Um humanizer não é obrigatório; este pacote não o inclui nem o instala.

Os skills continuam sujeitos às permissões e regras de aprovação do seu assistente. Eles não concedem acesso a contas nem autorizam gastos, envios, instalações ou publicações.

Compartilhe com o assistente escolhido apenas material que você tenha o direito de compartilhar. Confira as condições de tratamento de dados antes de fornecer informações confidenciais ou pessoais.

## Licença e procedência

[MIT](LICENSE). Copyright (c) 2026 Eugene Tsarkov. Desenvolvidos com assistência do OpenAI Codex.

Consulte a [procedência](PROVENANCE.md) para conhecer o histórico de desenvolvimento e os trabalhos relacionados conhecidos. O crédito de autoria cobre estas implementações mantidas; não reivindica a invenção dos métodos gerais de perguntas ou checagem de fatos.

O nome do autor, o link para o SetupKit, o identificador MIT e o texto completo da licença também permanecem em cada SKILL.md, acompanhando uma cópia independente.

O inglês é a fonte de referência. As traduções dos README descrevem os mesmos skills; cada skill tem um único SKILL.md em inglês.
