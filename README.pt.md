# SetupKit

[English](README.md) · [Español](README.es.md) · Português (Brasil) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Ajude sua IA a entender como você trabalha. Um guia gratuito ajuda você a definir regras de trabalho e avançar em uma tarefa real no seu próprio chat de IA.

## Como começar

1. Copie o [prompt inicial](prompts/pt.txt).
2. Cole no seu chat de IA e envie. Peça que a conversa seja em português do Brasil.
3. Responda às perguntas relevantes e escolha uma tarefa para trabalhar em conjunto.

Você pode começar no chat que já usa. Diga ao assistente qual ferramenta usa e como a utiliza. Se uma tarefa precisar de acesso adicional, confira primeiro o que seu chat pode fazer. Você pode continuar manualmente, deixar a etapa para depois ou escolher outro modo de trabalho. Instalar um aplicativo, por si só, não garante as ferramentas de que você precisa.

## Edição atual

[O guia completo](COMPLETE.md) está na edição `0.19`, atualizada em `2026-10-19`. Seu assistente deve fazer perguntas relevantes, explicar por que elas importam e aproveitar as respostas que você já deu.

Se não conseguir ler a fonte, siga as [etapas para fornecer o texto completo](docs/getting-started.md#if-the-guide-cannot-be-read). O conteúdo que faltar deve ser solicitado, não inventado. A página [Compatibilidade e limites](docs/compatibility.md) explica o que foi verificado e o que não foi. Esses documentos de referência e o guia original estão em inglês.

## Organização e contexto opcionais

Se for útil, você também pode organizar seu espaço de trabalho atual e preparar um pequeno conjunto de arquivos revisados sobre você, seus objetivos e seu trabalho. Comece com materiais que já tenha, como um currículo ou notas dos projetos que escolher. Você decide quais mudanças fazer; pode pular perguntas ou deixá-las para depois.

Ao retomar o trabalho, forneça o progresso salvo ou o resumo para continuar, para que seu assistente possa reutilizar as respostas confirmadas e revisar as etapas pendentes ou novas que sejam relevantes. Os arquivos só são salvos com sua aprovação e com o acesso que seu assistente realmente tiver; criá-los não garante memória nem sincronização automáticas.

## Organize materiais selecionados, se for útil

Peça ao seu assistente para ajudar a organizar arquivos, links ou anotações que você escolher. Ele pode sugerir a qual projeto cada material pertence, onde guardá-lo e o que vale resumir, mantendo referências aos originais. Revise a proposta e escolha o que mudar ou deixar para depois. Arquivos só são salvos ou movidos com sua aprovação e o acesso necessário; caso contrário, você recebe um plano para seguir manualmente. Ao retomar o trabalho, traga o registro revisado para que o assistente se concentre nos materiais novos, alterados ou pendentes.

## Skills

- [Clarify](skills/setupkit-clarify/README.pt.md): faz perguntas objetivas para esclarecer uma tarefa antes de começar.
- [Fact Check](skills/setupkit-fact-check/README.pt.md): revisa afirmações, evidências de apoio e requisitos de mídia antes da publicação.

Para instalar os dois, leia primeiro o [guia geral de instalação](INSTALL.pt.md) e confira as pastas de skills existentes. Para a primeira tentativa, use um projeto de teste novo e vazio.

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Escolha o assistente e o escopo do projeto; revise os destinos antes de confirmar. npx executa o instalador. Veja [a apresentação dos skills](skills/README.pt.md) para os limites de compatibilidade e as instruções de instalação individual.

## Seu trabalho fica com você

Não é preciso ter uma conta no SetupKit. O SetupKit não recebe as respostas que você dá ao assistente. Valem os custos, as permissões e as regras de tratamento de dados do seu assistente. Pedir um rascunho não autoriza enviar, publicar, instalar, conectar uma conta ou alterar arquivos.

## Autoria e reutilização

Criado por [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Um projeto independente e gratuito. O texto do guia está sob a licença [CC BY 4.0](LICENSE.md), que permite compartilhar e adaptar, inclusive comercialmente, conforme suas condições. Dê crédito, inclua links para o guia original e a licença e indique as alterações conforme exigido. Os sete textos de apoio indicados em LICENSE.md seguem as mesmas condições CC BY 4.0. A configuração do repositório não faz parte dessa autorização. Nenhuma licença para código, logotipos ou materiais de terceiros está implícita.

## Feedback e idioma

Veja as [orientações de contribuição](CONTRIBUTING.md) e [como relatar problemas de segurança](SECURITY.md). Não publique conversas privadas, arquivos ou segredos em uma issue do GitHub. O inglês é a fonte de referência; a conversa guiada pode ser no idioma que você escolher. As versões do site só serão apresentadas como disponíveis depois da revisão de todo o percurso em cada idioma.
