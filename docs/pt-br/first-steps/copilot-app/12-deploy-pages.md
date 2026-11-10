---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Dê ao Space Quiz um endereço público publicando-o com o GitHub Pages. O Copilot pode preparar o fluxo de trabalho e orientar a publicação, mas você é responsável por revisar as mudanças e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar uma publicação no GitHub Pages.
- revisar o fluxo de trabalho e o pull request antes de fazer o merge.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma forma simples de experimentá-lo. Publicar o site de um único arquivo com o GitHub Pages o disponibiliza em uma URL pública, sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um fluxo de trabalho do GitHub Actions que compile o site, se necessário, e o publique no GitHub Pages. Adicione um README que descreva o aplicativo e explique como executá-lo localmente, caso ainda não exista. Crie um pull request com essas mudanças e faça o merge depois que as verificações obrigatórias forem aprovadas. Monitore a publicação até que ela seja concluída e, em seguida, informe a URL final do site. Se você não tiver permissão para habilitar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que a tarefa foi concluída até que o site esteja no ar.
```

![Diagrama em três etapas: pull request do Space Quiz mesclado; execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça merge de um pull request e altere as configurações do Pages do repositório. Revise as diferenças, as permissões de publicação e qualquer solicitação de aprovação do GitHub antes de continuar.

## Revise o fluxo de trabalho e verifique a publicação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as mudanças do pull request, incluindo as etapas de build e publicação do fluxo de trabalho.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de publicação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz é carregado.

Se o agente não conseguir habilitar o Pages ou fazer o merge do pull request, siga as instruções específicas que ele fornecer. Não considere a tarefa concluída até que a publicação seja bem-sucedida e o site esteja acessível.

## Resumo e próximos passos

O Space Quiz agora está disponível como um site publicado, e você verificou a implantação em vez de depender do relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
