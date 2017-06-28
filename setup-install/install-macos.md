# Configuração e instalação de ambiente - Mac OS Sierra / OS X

### Instalando e configurando o `Java`
1. __Instalação do `Java`__
    
    Você pode instalar o Java por [aqui](http://www.oracle.com/technetwork/pt/java/javase/downloads/jdk8-downloads-2133151.html).
    
2. __Alteração do `$PATH`__

    As instruções oficiais para alteração da varável $PATH são essas [aqui](https://www.java.com/pt_BR/download/help/path.xml).

### Clonando o repositório
Recomendo utilização do [GitKraken](http://gitkraken.com/) para melhor visualização do projeto no GitHub, e notificações sobre o estado do projeto. Com ele você deve dar um fork no meu projeto no GitHub e cloná-lo para a sua máquina.

Caso prefira fazer isso pelo terminal, navegue até o diretório em que você deseja que fique o projeto e clone o repositório com:
```shell
    git clone https://github.com/izabelacborges/test-automation-java-setup.git
```

### Instalando o Chrome e o ChromeDriver:
1. __Chrome__

Este passo só deve ser reproduzido caso você não tenha o Chrome instalado em seu computador.

Instale o Chrome browser clicando [aqui](https://www.google.com/chrome/index.html).

2. __ChromeDriver__

```shell
brew install chromedriver
```
Se aparecer uma mensagem `"Warning: chromedriver already installed, it's just not linked"` execute o comando:
```shell
brew link --overwrite chromedriver
```
Se você está usando o Sierra pode passar por alguns problemas de permissão, para mudar as permissões de usuário, use:
```shell
sudo chown -R (whoami) /usr/local
```
refaça a instalação e o link (caso necessário) e volte a permissão de usuário para o padrão com:
```shell
sudo chown root:wheel /usr/local
```

### selenium-server-standalone
Para rodar os testes será necessário ter o selenium server. Você pode baixar o arquivo `.jar` [aqui](https://goo.gl/s4o9Vx).

Antes de executar os testes você precisa rodar o arquivo `.jar` com:
```shell
java -jar selenium-server-standalone-3.4.0.jar
```

### Apache Maven e JUnit
1. __Apache Maven__

    Você pode fazer o download do Maven por [aqui](https://maven.apache.org/download.cgi), e instalá-lo com [estes passos](https://maven.apache.org/install.html).

2. __JUnit__

    Para fazer o download do JUnit, você deve baixar os arquivos `.jar` descritos [aqui](https://github.com/junit-team/junit4/wiki/Download-and-Install). __NÃO É NECESSÁRIO__ seguir os outros passos, pois iremos passar por eles na parte prática do curso.

### IntelliJ IDEA IDE
Neste projeto foi usado o IntelliJ IDEA. Você pode instalá-lo por [aqui](https://www.jetbrains.com/idea/download/).