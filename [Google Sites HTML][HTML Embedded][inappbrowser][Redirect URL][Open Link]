# Introdução

Meus cumprimentos a todos **integrantes da comunidade**.
Venho **humildemente** até vocês para sanar algumas dúvidas a respeito de códigos embutidos (**embuded html code**) dentro de sites google - https://sites.google.com/


# Contexto

Estou usando a plataforma do **google sites** para o desenvolvimentos de páginas na web e então surgiram alguma dúvidas a respeito do **código HTML embutido** que o sites google permite inserir dentro de suas próprias páginas.

Ao utilizar elementos nativos da plataforma como por exemplo o objeto **Botão** ou objeto **Imagem** dentro da plataforma do google site, percebemos
que é possível **inserir urls** para links internos ou externos. 

Porem ao usar o recurso de **"HTML EMBUTIDO"** o código parece ficar envelopado em formato de **frame** e eu não consigo fazer **redirecionamentos externos** a partir dele.

**Por exemplo**, se eu criar inserir um botão através desse recurso "embuded html code" , o máximo que eu consigo fazer é um **redirecionamento da url interna** do frame. Não consigo **sair do frame** com um evento de um botão que me leve para uma página externa, exemplo: www.facebook.com

Exemplo ilustrado <<<<<<<
[FOTO1 - Página Site Goole][Mostrar o HTML embedded]

Com base nesse contexto, **vou explicar melhor** minha dúvida na seção  abaixo.

# Mínha Dúvida - Meu Problema

A minha dúvida está relacionada a uso do **recurso "embuded html code".** 

Seria possível criar um evento a partir do frame interno e fazer um redirecionando de url para uma página externa?

> ##### Observação importantissima:  Levar em consideração os teste em um in app browser - ou seja, se o recurso funcionar dentro do browser nativo do instagram por exemplo, então teremos encontrado a solução. 

## Minhas Tentativas de Solução

Levando em consideração as minhas pesquisas para **resolver o problema**, segue **algumas tentativas** realizadas

**Tentativa 0** - Consigo acessar um url externa mas ela abre dentro do próprio frame  ( **não resolve minha questão** =\ )
```
<button onclick="window.location.href='https://trafegolocalsimples.us7.list-manage.com/subscribe/post?u=a5e8cfba5cbc7735672bd3138&amp;id=a5e847aef3';" target="_parent" > Redirect form mailchimp inside frame - target="_parent" </button>
<br><br>
<button onclick="window.location.href='https://trafegolocalsimples.us7.list-manage.com/subscribe/post?u=a5e8cfba5cbc7735672bd3138&amp;id=a5e847aef3';" target="_top" > Redirect form mailchimp inside frame - target="_top </button>
<br>
```
Exemplo ilustrado <<<<<<<
[FOTO2 - Imagem site google rederizando o formulário dentro do page google]
. 
Possível acompanhar o exemplo na página a seguir - https://sites.google.com/view/stackoverflow-example-redirect/

---
**Tentativa 1** -  Acessar o elemento Pai do frame para poder fazer o redirecionamentos no frame principal.

**Code example**
 ```
 <button onclick="window.top.location.href = 'http://google.com';">Redirect Top</button>
```

Nesse caso eu recebo uma **mensagem de erro no log** do browser.
Teoricamente, Através do recurso javascript - **window.top.location.href** deveria ser possível acessar o elemento pai e fazer o redirecionamento, porem a 

A seguir vem a **Mensagem de error:**
> The frame attempting navigation of the top-level window is sandboxed, but the flag of 'allow-top-navigation' or 'allow-top-navigation-by-user-activation' is not set.

Exemplo ilustrado <<<<<<<
[FOTO3 - Imagem debug error]

Após receber essa mensagem de erro eu fui para a próxima tentativa com ajuda do link abaixo.
###### Fonte:https://stackoverflow.com/questions/580669/redirect-parent-window-from-an-iframe-action
.
**Tentativa 2** - Fornecer permissão ao frame através da tag - ```<iframe src="about:blank" sandbox="allow-top-navigation,allow-scripts"> ```

Após ler a fonte acima para resolver o problema, tentei editar manualmente a **propriedade sandbox="allow-top-navigation"** para  permitir que o frame filho tenha acesso a elementos do frame pai com objetivo de conseguir fazer o **redirecionamento da página**, porem a mensagem de error é exibida:


**Code example**
````
<iframe src="about:blank" sandbox="allow-top-navigation,allow-scripts"> </iframe>

<button onclick="window.parent.location.href = 'http://google.com';">Redirect Top with parent</button>
````

A seguir vem a **Mensagem de error:**
>Unsafe JavaScript attempt to initiate navigation for frame with URL '...'
The frame attempting navigation is sandboxed, and is therefore disallowed from navigating its ancestors.

Exemplo ilustrado<<<<<<<
[FOTO4 - Imagem debug error - sandbox updated ]
Possível acompanhar o exemplo na página a seguir - https://sites.google.com/view/stackoverflow-example-redirect/


# Conclusão

**Estou ciente** que uma resposta possível é:
- Alternativa 1 : **Não é possível fazer o redirecionamento** pois não tenho permissão para acessar elementos fora do frame dentro do contexto de page site google.
- Alternativa 2 : Só é possível fazer o redirecionamento se você tiver **acesso ao servidor** - ou seja - Necessário ter o próprio site, nos sites do google não é possível.
.
Apesar de todas as minhas tentativas apontarem para a resposta ser **problemas de fato com permissão**, Gostaria de confirmar essas suspeitas com a comunidade.
Espero poder ter trazido **clareza** a pergunta e me disponho a fazer as edições necessárias no post quando necessário.
.
##### As ilustrações desse link me ajudaram a entender um pouco sobre a arquitetura dos frames - https://rainmakerho.github.io/2020/07/21/2020012/
.
###### fonte extra : https://html.spec.whatwg.org/multipage/origin.html#forced-sandboxing-flag-set
