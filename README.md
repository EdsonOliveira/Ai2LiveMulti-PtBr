Ai2LiveMulti-PtBr
=================

Fork of Ai2LiveComplete de M. Hossein Amerkashi - Translate do PtBr

#Benvindo ao MIT App Inventor

##Introdução

Entenda mais sobre o [MIT App Inventor](http://appinventor.mit.edu).

Este código foi desenhado para rodar no engine Gogle's App. MIT executa
em uma instância pública onde todos são benvindos a ajudar no 
desenvolvimento do aplicativo App Inventor, mas não precisa compilar ou 
usar este código para ajudar.

Este código é liberado para referência e para pessoas experientes que
querem operar seus aplicativos e/ou contribuir para o projeto.

Este código foi testado para usar com Java 7.

##Contribuidores
A melhor maneira de se integrar com as alteraçõe sé se registrar no  [Open Source forum](https://groups.google.com/forum/#!forum/app-inventor-open-source-dev) e informar o que deseja alterar.

Utilizamos documentos com características ** breves e informais ** com a descrição das mudanças e telas de como deve ser o funcionamento das propostas, assim permitindo reunir mais rápido o máximo de feedback da comunidade. Geralmente é usado o compartilhamento via Google docs (com permissão de adicinar comentários), mas pode ser utilizado outro meiro que permita adição de comentários.

Se você pulou este passo e ter iniciado suas alterações fique a vontade para se linkar mas poderemos pedir que volte e documente-as. Lembre-se que o objetivo principal disso é reunir o máximo de feedback, o mais cedo possível. Iremos também possivelmente pedir para você colocar uma instância com as alterações no [appspot](http://appspot.com), e fornecer um aplicativo Coletivo modificado (se aplicável), para que os revisores podem usar as mudanças antes de analisar para a fonte.

Confirna nosso open source original [site](http://appinventor.mit.edu/appinventor-sources/) ou esta versão [site](https://github.com/EdsonOliveira/appinventor-sources-PtBr/) para encontrar mais informações sobre o projeto e como contribuir.

##Instruções de Setup

Existe um guia breve de como iniciar com os fontes. Instruções mais detalhadas podem ser encontradas em [aqui](https://docs.google.com/document/pub?id=1Xc9yt02x3BRoq5m1PJHBr81OOv69rEBy8LVG_84j9jc), uma apresentação pode ser vista [aqui](http://josmas.github.io/contributingToAppInventor2/#/), e toda a [documentação](http://appinventor.mit.edu/appinventor-sources/#documentation) original pode ser encontrada em no [site](http://appinventor.mit.edu/appinventor-sources/).

###Dependências
Você vai precisar do Java JDK full (6 or 7, de preferencia da Oracle; JRE não é o suficiente) e Python para compilar e rodar o server.

Você precisa também da cópia do [App Engine SDK](https://developers.google.com/appengine/downloads) para java e o [ant](http://ant.apache.org/) do apache.

Se você quer fazer alterações nos fontes, você terá que usar uma suite de testes automáticos, poderá ser o [phantomjs](http://phantomjs.org/). Dê uma olhada na seção de testes para maior informações.

###Forking or cloning (Modificando ou Clonando)
Considere ***forking*** o projeto que você faz alterações nos fontes. Se simplesmente for rodar localmente, chame de ***clone***

####Forking (Modificando)
Se decidir modificar, siga as [instruções](https://help.github.com/articles/fork-a-repo) do github. Após isto, você pode pegar uma copia de nossos fontes com:

    $ git clone https://github.com/YOUR_USER_NAME/SEU_PROJETO.git

Coloque em *YOUR_USER_NAME* o seu nome de cadastro.
Coloque em *SEU_PROJETO* o nome de seu projeto.

Configurar um ponto remoto para este repositório é uma boa idéia se você estiver forkando.

    $ cd SEU_PROJETO
    $ git remote add upstream https://github.com/mit-cml/appinventor-sources.git

Finalmente, você deverá ter o cuidado de ignorar os arquivos que devem ser ignorados.

    $ cp sample-.gitignore .gitignore


###Compilando
É muito simples compilar se tiver todas as dependências; basta abrir o terminal e digitar:

    $ cd SEU_PROJETO
    $ ant

Seu terminal irá operar e code até ter umas pausas por alguns minitos (depende de sua máquina) e no final irá ver algo como *Build Successful*.

###Executando o servidor
Existem dois sedrvidores no App Inventor, o *main server* que detalha as informações do projeto, e o *build server* que cria os arquivos apk. Mais detalhes podem ser encontrados no documento [App Inventor Developer Overview](https://docs.google.com/document/d/1hIvAtbNx-eiIJcTA2LLPQOawctiGIpnnt0AvfgnKBok/pub).

####Executando o the main server

    $ your-appengine-SDK-folder/bin/dev_appserver.sh
            --port=8888 --address=0.0.0.0 appengine/build/war/

modifique o appengine para o seu *your-appengine-SDK-folder* de acordo com o lugar que armazenou  seu App Engine SDK.

####Executando o build server
O build server pode ser executado digitando no terminal:

    $ cd appinventor/buildserver
    $ ant RunLocalBuildServer

Observe que somente irá executar o build server se você estiver construindo um app como um apk. Você terá todas as funções para programar sem ter que todar o build server, mas precisará dele para construir o apk.

###Acessando seu servidor local
Você pode agora ativar e executar; pode testá-lo chamando no seu broeser:

    http://localhost:8888

###Executando testes
O teste automático depende de [Phantomjs](http://phantomjs.org/). Certifique-se que o instalou e será encontrado no path. Você pode rodar os testes chamando no terminal:

    $ ant tests

##Precisa de ajuda?
Contate-nos pelo nosso [Google Group](https://groups.google.com/forum/#!forum/app-inventor-open-source-dev) or [G+ community](https://plus.google.com/u/0/b/116831753302186936352/116831753302186936352/posts).