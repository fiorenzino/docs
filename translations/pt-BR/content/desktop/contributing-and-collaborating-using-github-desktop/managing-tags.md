---
title: Gerenciar tags
intro: 'Você pode usar {{ site.data.variables.product.prodname_desktop }} para criar, fazer push e visualizar tags.'
redirect_from:
  - /desktop/contributing-to-projects/managing-tags
versions:
  free-pro-team: '*'
---

### Sobre tags no {{ site.data.variables.product.prodname_desktop }}

O {{ site.data.variables.product.prodname_desktop }} permite que você crie tags anotadas. É possível usar uma tag para marcar um ponto individual no histórico do seu repositório, incluindo um número de versão para uma versão. Para obter mais informações sobre tags de versão, consulte "[Sobre versões](/github/administering-a-repository/about-releases)"

{{ site.data.reusables.desktop.tags-push-with-commits }}

### Criar uma tag

{{ site.data.reusables.desktop.history-tab }}
{{ site.data.reusables.desktop.create-tag }}
{{ site.data.reusables.desktop.name-tag }}
{{ site.data.reusables.desktop.confirm-tag }}

### Visualizar tags

{{ site.data.reusables.desktop.history-tab }}
2. Clique em commit.
  {% note %}

  **Observação**: {{ site.data.variables.product.prodname_desktop }} exibe uma seta {% octicon "arrow-up" aria-label="The up arrow icon" %} se a tag não foi tiver sido empurrada para o repositório remoto.

  {% endnote %}

  ![Visualizar uma tag no histórico](/assets/images/help/desktop/viewing-tags-in-history.png)

3. Todas as tags associadas ao commit são visíveis nos metadados desse commit. ![Visualizar uma tag no commit](/assets/images/help/desktop/viewing-tags-in-commit.png)