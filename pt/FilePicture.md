Primeiro cabeçalho | Segundo cabeçalho
--- | ---
Célula de conteúdo | Célula de conteúdo
Célula de conteúdo | Célula de conteúdo

Primeiro cabeçalho | Segundo cabeçalho
--- | ---
Célula de conteúdo | Célula de conteúdo
Célula de conteúdo | Célula de conteúdo

![Cidadela](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Esquerda alinhada | Alinhado ao centro | Alinhado à direita
:-- | :-: | --:
coluna 3 é | algum texto prolixo | **US$ 1.600**
coluna 2 é | centrado | US$ 12
listras de zebra | são legais | ~~$1~~

Dillinger is a cloud-enabled, mobile-ready, offline-storage, AngularJS powered HTML5 Markdown editor.

- Digite algum Markdown à esquerda
- Veja HTML à direita
- Magia 1

# verdadeiro

- Importe um arquivo HTML e veja-o ser convertido magicamente para Markdown
- Arraste e solte imagens (requer que sua conta do Dropbox esteja vinculada) f

Você também pode: 2

- Importe e salve arquivos do GitHub, Dropbox, Google Drive e One Drive
- Arraste e solte markdown e arquivos HTML no Dillinger
- Exporte documentos como Markdown, HTML e PDF

Markdown é uma linguagem de marcação leve baseada nas convenções de formatação que as pessoas usam naturalmente em emails. Como [John Gruber] escreve no [site Markdown][df1] 12

> O principal objetivo de design da sintaxe de formatação do Markdown é torná-la o mais legível possível. A ideia é que um documento formatado em Markdown possa ser publicado como está, como texto simples, sem parecer que foi marcado com tags ou instruções de formatação.

Este texto que você vê aqui está, *na verdade* , escrito em Markdown! Para ter uma ideia da sintaxe do Markdown, digite algum texto na janela esquerda e observe os resultados à direita. 31

### falso 22

Dillinger usa vários projetos de código aberto para funcionar corretamente:

- [AngularJS] - HTML aprimorado para aplicativos da web!
- [Ace Editor] - incrível editor de texto baseado na web
- [markdown-it] - Analisador de Markdown bem feito. Rápido e fácil de estender.
- [Twitter Bootstrap] - excelente padrão de UI para aplicativos da web modernos
- [node.js] - E/S com eventos para o back-end
- [Express] - estrutura rápida de aplicativo de rede node.js [@tjholowaychuk]
- [Gulp] - o sistema de compilação de streaming
- [Breakdance](https://breakdance.github.io/breakdance/) - conversor de HTML para Markdown 23
- [jQuery] - duh

E é claro que o próprio Dillinger é de código aberto com um [repositório público] [dill] no GitHub.

### Instalação 32

![Ilos](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg) 24

Dillinger requer [Node.js](https://nodejs.org/) v4+ para ser executado.

Instale as dependências e devDependencies e inicie o servidor.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Para ambientes de produção...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plug-ins

Dillinger está atualmente estendido com os seguintes plugins. As instruções sobre como usá-los em seu próprio aplicativo estão no link abaixo. 33

Plugar | Leia-me
--- | ---
Dropbox | [plugins/dropbox/README.md][PlDb]
GitHub | [plugins/github/README.md][PlGh]
Google Drive | [plugins/googledrive/README.md][PlGd]
OneDrive | [plugins/onedrive/README.md][PlOd]
Médio | [plugins/medium/README.md][PlMe]
Google Analytics | [plugins/googleanalytics/README.md][PlGa]

### Desenvolvimento

Quer contribuir? Ótimo!

Dillinger usa Gulp + Webpack para desenvolvimento rápido. Faça uma alteração no seu arquivo e veja instantaneamente suas atualizações!

Abra seu Terminal favorito e execute estes comandos.

Primeira guia:

```sh
$ node app
```

Segunda guia:

```sh
$ gulp watch
```

(opcional) Terceiro:

```sh
$ karma test
```

#### Construindo para fonte

Para liberação de produção:

```sh
$ gulp build --prod
```

Gerando arquivos zip pré-construídos para distribuição:

```sh
$ gulp build dist --prod
```

### Docker

Dillinger é muito fácil de instalar e implantar em um contêiner Docker.

Por padrão, o Docker irá expor a porta 8080, então altere isso no Dockerfile, se necessário. Quando estiver pronto, basta usar o Dockerfile para construir a imagem.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Isso criará a imagem dillinger e extrairá as dependências necessárias. Certifique-se de trocar `${package.json.version}` pela versão real do Dillinger.

Uma vez feito isso, execute a imagem Docker e mapeie a porta para o que desejar em seu host. Neste exemplo, simplesmente mapeamos a porta 8000 do host para a porta 8080 do Docker (ou qualquer porta exposta no Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verifique a implantação navegando até o endereço do servidor no navegador de sua preferência.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

Veja [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Todos
