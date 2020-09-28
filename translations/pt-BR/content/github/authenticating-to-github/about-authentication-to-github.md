---
title: Sobre a autenticação no GitHub
intro: 'Você pode acessar com segurança os recursos da sua conta efetuando a autenticação no {{ site.data.variables.product.product_name }} e usando credenciais diferentes dependendo de onde você efetua a autenticação.'
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

### Sobre autenticação no {{ site.data.variables.product.prodname_dotcom }}

Para manter sua conta segura, você deve efetuar a autenticação antes de acessar certos recursos no {{ site.data.variables.product.product_name }}. Ao efetuar a autenticação em {{ site.data.variables.product.product_name }}, você fornece ou confirma credenciais que são exclusivas que provam quem você declara ser.

Você pode acessar seus recursos em {{ site.data.variables.product.product_name }} de várias formas: no navegador, por meio do {{ site.data.variables.product.prodname_desktop }} ou outro aplicativo da área de trabalho, com a API ou por meio da linha de comando. Cada forma de acessar o {{ site.data.variables.product.product_name }} é compatível com diferentes modos de autenticação.

- O nome de usuário e a senha com autenticação de dois fatores
- Token de acesso de pessoal
- Chave SSH


### Efetuar a autenticação no seu navegador

Você pode efetuar a autenticação no {{ site.data.variables.product.product_name }} no seu navegador de diferentes formas.

- **Apenas nome de usuário e senha**
    - Você criará uma senha ao criar sua conta de usuário em {{ site.data.variables.product.product_name }}. Recomendamos que você use um gerenciador de senhas para gerar uma senha aleatória e única. Para obter mais informações, consulte "[Criar uma senha forte](/github/authenticating-to-github/creating-a-strong-password)".
- **Autenticação de dois fatores (2FA)** (recomendado)
    - Se você habilitar a 2FA, também iremos solicitar que você forneça um código gerado por um aplicativo no seu dispositivo móvel ou enviado como uma mensagem de texto (SMS) depois que você digitar seu nome de usuário e senha com sucesso. Para obter mais informações, consulte "[Acessar o {{ site.data.variables.product.prodname_dotcom }} usando a autenticação de dois fatores](/github/authenticating-to-github/accessing-github-using-two-factor-authentication#providing-a-2fa-code-when-signing-in-to-the-website)".
    - Além de autenticação com um aplicativo para celular ou uma mensagem de texto. você pode, opcionalmente, adicionar um método secundário de autenticação com uma chave de segurança usando o WebAuthn. Para obter mais informações, consulte "[Configurar a autenticação de dois fatores usando uma chave de segurança](/github/authenticating-to-github/configuring-two-factor-authentication#configuring-two-factor-authentication-using-a-security-key)".

### Efetuar a autenticação com {{ site.data.variables.product.prodname_desktop }}

Você pode efetuar a autenticação com o {{ site.data.variables.product.prodname_desktop }} usando seu navegador. Para obter mais informações, consulte "

Autenticar-se no {{ site.data.variables.product.prodname_dotcom }}."</p> 



### Efetuar a autenticação com a API

Você pode efetuar a autenticação com a API do {{ site.data.variables.product.product_name }} de formas diferentes.

- **Tokens de acesso pessoal** 
      - Em algumas situações, como, por exemplo, testes, você pode usar um token de acesso pessoal para acessar a API. Usar um token de acesso pessoal permite que você revogue o acesso a qualquer momento. Para mais informação, consulte "[Criando um token de acesso pessoal](/github/authenticating-to-github/creating-a-personal-access-token)."
- **Fluxo do aplicativo web** 
      - Para aplicativos OAuth em produção, você deve efetuar a autenticação usando o fluxo do aplicativo web. Para obter mais informações, consulte "[Autorizar aplicativos OAuth](/apps/building-oauth-apps/authorizing-oauth-apps/#web-application-flow)".
- **Aplicativos do GitHub** 
      - Para aplicativos GitHub em produção, você deve efetuar a autenticação em nome da instalação do aplicativo. Para obter mais informações, consulte "[Efetuando a autenticação com o {{ site.data.variables.product.prodname_github_apps }}](/apps/building-github-apps/authenticating-with-github-apps/)".



### Efetuando a autenticação com a linha de comando

Você pode acessar repositórios no {{ site.data.variables.product.product_name }} pela linha de comando de duas maneiras, HTTPS e SSH. Ambos têm uma maneira diferente de efetuar a autenticação. O método de autenticação é determinado com base na escolha de uma URL remota de HTTPS ou SSH quando você clonar o repositório. Para obter mais informações sobre qual forma de acesso, consulte "[Qual URL remota devo usar?](/github/using-git/which-remote-url-should-i-use)"

* Você pode trabalhar com todos os repositórios no {{ site.data.variables.product.product_name }} por meio de HTTPS, mesmo que você esteja atrás de um firewall ou proxy. Sempre que você usar o Git para efetuar a autenticação com {{ site.data.variables.product.product_name }}, será solicitado que você insira suas credenciais para efetuar a autenticação com {{ site.data.variables.product.product_name }}, a não ser que você os armazene com um [auxiliar de credenciais](/github/using-git/caching-your-github-credentials-in-git). {{ site.data.reusables.user_settings.password-authentication-deprecation }}

* Você pode trabalhar com todos os repositórios no {{ site.data.variables.product.product_name }} por meio de SSH, embora os firewalls e proxys possam se recusar a permitir conexões de SSH. Usar o SSH exige que você gere um par de chave pública/privada de SSH no seu computador local e adicione a chave pública à sua conta de {{ site.data.variables.product.product_name }}. Sempre que usar o Git para efetuar a autenticação com {{ site.data.variables.product.product_name }}, será solicitado que você digite a senha da sua chave SSH, a menos que você [tenha armazenado a chave](/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent). Para obter mais informações, consulte "[Gerar uma nova chave SSH e adicioná-la ao ssh-agent](/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)".

{% if currentVersion == "free-pro-team@latest" %}Para usar um token de acesso pessoal ou chave SSH para acessar os recursos que pertencem a uma organização que usa o logon único SAML, você também deve autorizar o token pessoal ou chave SSH. Para obter mais informações consulte "[Autorizar um token de acesso pessoal para usar com logon único SAML](/github/authenticating-to-github/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on)" ou "[Autorizando uma chave SSH para uso com o logon único SAML](/github/authenticating-to-github/authorizing-an-ssh-key-for-use-with-saml-single-sign-on).{% endif %}