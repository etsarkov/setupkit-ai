# SetupKit Fact Check

Autor: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · Licença: **MIT**

[English](README.md) · [Español](README.es.md) · Português (Brasil) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Revise afirmações e evidências antes da publicação.

## Quando usar

Use o Fact Check quando um texto público estiver pronto para revisão factual ou quando você pedir explicitamente a verificação de uma afirmação. Ele separa fatos, experiência pessoal, opiniões e hipóteses, verifica as evidências disponíveis e entrega um registro compacto de afirmações.

A decisão é PASS, PASS WITH EDITS ou BLOCK. Afirmações essenciais sem respaldo ou requisitos importantes de mídia ainda não resolvidos levam a BLOCK.

## Instalação

Leia primeiro as instruções do skill. Para a primeira tentativa, use um projeto de teste novo e vazio. Antes de executar o comando, verifique se já existem pastas do skill nos destinos e locais compartilhados do projeto; decida qualquer atualização separadamente. Consulte o [guia geral de instalação](../../INSTALL.pt.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Escolha o assistente de destino e o escopo do projeto. Revise as opções pré-selecionadas, os destinos e o resumo final antes de confirmar. Alguns assistentes compartilham .agents/skills; outros assistentes do projeto podem descobrir os arquivos colocados ali.

npx baixa e executa o instalador. O guia comum de instalação informa as versões e os modos testados e os limites de compatibilidade.

## Exemplos

Trechos e dados fictícios, não afirmações sobre empresas reais, resultados medidos ou direitos sobre imagens.

### Preservar o sentido de uma citação

**Material para verificar:**

```text
Use setupkit-fact-check. Trecho fictício da fonte: “Estamos considerando um lançamento em junho”. Rascunho: “A empresa lançou o produto”.
```

**Resultado ilustrativo:** Identifica que um possível lançamento futuro virou um fato concluído. Substitui a afirmação por uma atribuição fiel, como “A empresa diz que está considerando um lançamento em junho”. Confere qualquer citação final com a fonte fornecida.

### Conferir porcentagens

**Material para verificar:**

```text
Use setupkit-fact-check. Dados fictícios fornecidos: antes, 10 conversões em 100 visitas; depois, 12 em 100. Rascunho: “A conversão aumentou 20 pontos percentuais”.
```

**Resultado ilustrativo:** Corrige para “A conversão passou de 10% para 12%: 2 pontos percentuais, ou um aumento relativo de 20%”. PASS WITH EDITS para este exemplo aritmético após conferir a correção; os números não comprovam uma medição real, significância estatística ou causalidade.

### Verificar a procedência de uma foto

**Material para verificar:**

```text
Use setupkit-fact-check. Um post inclui uma foto encontrada na internet. O autor, a fonte original e a permissão para esse uso são desconhecidos.
```

**Resultado ilustrativo:** Registra a falta de procedência e de permissão. BLOCK enquanto requisitos importantes de mídia aplicáveis permanecerem sem resolução. Pede a fonte e a permissão ou substitui a imagem por outra cujo uso pretendido esteja respaldado.

## Limites

A revisão depende das fontes e ferramentas disponíveis para o seu assistente. Fatos sujeitos a mudança precisam de verificação atual. PASS avalia o texto e as evidências verificados; não autoriza a publicação nem substitui orientação profissional quando necessária.

Os skills continuam sujeitos às permissões e regras de aprovação do seu assistente. Eles não concedem acesso a contas nem autorizam gastos, envios, instalações ou publicações.

Compartilhe com o assistente escolhido apenas material que você tenha o direito de compartilhar. Confira as condições de tratamento de dados antes de fornecer informações confidenciais ou pessoais.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.pt.md)

## Licença e procedência

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Desenvolvidos com assistência do OpenAI Codex.

Consulte a [procedência](../PROVENANCE.md) para conhecer o histórico de desenvolvimento e os trabalhos relacionados conhecidos. O crédito de autoria cobre estas implementações mantidas; não reivindica a invenção dos métodos gerais de perguntas ou checagem de fatos.

O nome do autor, o link para o SetupKit, o identificador MIT e o texto completo da licença também permanecem em cada SKILL.md, acompanhando uma cópia independente.

O inglês é a fonte de referência. As traduções dos README descrevem os mesmos skills; cada skill tem um único SKILL.md em inglês.
