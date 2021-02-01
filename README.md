 <p align="center">
    <img src="./img/git-logo.png" alt="Logo do Git">
 </p>

---

# Guia de Git e GitHub para Iniciantes

Esse guia foi feito com o intuito de ajudar aqueles no qual nunca tiveram contato com GIT antes, porém caso já possua conhecimentos na ferramenta, também pode ser utilizado com o objetivo de relembrar a utilização de alguns comandos presentes no final desse README.

## Mas, na verdade, o que é GIT?

GIT é uma ferramenta de versionamento, através dessa ferramenta podemos fazer o controle de versões, controle de versões? Mas o que é isso? Você deve estar se perguntando, bom… Falando bem por cima mesmo, imagine o git como uma ferramenta de permite você registrar todos os acontecimentos durante um projeto, tendo em mente esses acontecimentos como as alterações feitas no código do projeto que você esteja trabalhando, a partir disso podemos usar o GIT para voltar no tempo em um determinado ponto do desenvolvimento, sabe quando você estava fazendo aquele trabalho da escola no computador, e quando pensou que terminou ele salvou como "trabalho de educação física", mas aí algum tempo depois o seu coleguinha te manda uma mensagem falando que você esqueceu de acrescentar algum conteúdo nele, com isso, lá vai você editar o seu trabalho, e quando feito salva ele como uma segunda versão "trabalho de educação 2.0",  e então você se encontra com dois arquivos, a diferença do seu trabalho para um projeto seja em qual for que esteja trabalhando, é que ele enfrentará diversas alterações, e às vezes essas alterações podem acabar danificando o resultado final, para isso podemos usar o GIT e voltar em pontos registrados na linha do tempo.

## Ok, meio que entendi o que é GIT, mas agora, e esse tal de GitHub?

Sendo bem direto ao ponto, o GitHub nada mais é do que uma plataforma online de hospedagem de códigos fonte juntamento com um controle de versionamento, através dele você pode expor seus projetos de maneira que toda a comunidade de programadores possam ler, ou até mesmo contribuir com a construção do resultado final, sabe, eu gosto de imaginar o GitHub como uma cozinha imensa com vários fogões, mesas, fornos, e vários cozinheiros preparando seus pratos, eu imagino os cozinheiros como os programadores, dispostos a preparar seus pratos, mas também a ajudar os colegas cozinheiros próximos com seus conhecimentos e práticas, o prato que está sendo feito é como se fosse o projeto, a diferença é que bom... Nossa cozinha gigante é a internet, e a maneira como podemos ajudar é através de contribuições que podem ser feitas através do versionamento.

---

## Tá, mas como eu começo a pôr a mão na massa então?

Bom primeiramente você deve instalar o GIT na sua máquina, que pode ser adquirido através desse <a href="https://git-scm.com/">link</a>, a instalação é bem fácil e prática, assim que instalado, você já será capaz de utilizar o mesmo localmente na sua máquina, basta abrir qualquer diretório, apertar com o botão direito em um espaço vazio e selecionar "Git Bash Here".

---

## Operações Locais

Antes de começarmos a utiliza a ferramente de vez, vamos falar um pouco sobre operações locais no git, basicamente temos três niveis de operações, são elas <strong>Working Directory</strong>, <strong>Staging Area</strong> e <strong>Git Directory (repositório)</strong>.

### Working Directory

Em primeiro nível, temos a working directory, é nesse local que o nosso projeto enfrentará uma série de inúmeras alterações e testes, é como se fosse o nosso brinquedo de lego onde montamos as peças como queremos até alcançar o resultado desejado.

### Staging Area

Staging directory, é aqui que muitas pessoas se perdem e não conseguem compreender a real função da Stage, imagine que você está trabalhando em um projeto X com duas funcionalidades, e no mesmo dia você fez alterações em ambas as funcionalidades, porém só conseguiu concluir uma e deixou a outra pela metade, você observa o horário e já chegou no final do seu expediente, como você não vai mais poder finalizar hoje, pretende enviar somente a funcionalidade que está completa, e é aí que entra a Stage Directory, é nela que você irá enviar apenas as alterações concluídas, que no final podem ser enviadas para a "linha do tempo", as alterações inacabadas, continuam na Working Directory,  saindo de lá apenas quando finalizadas.

### Git Directory

Enfim o Git Directory, a nossa linha do tempo, após ter inserido os itens finalizados na nossa Staging Directory, podemos passar todas as alterações concluídas com exito para a serem catalogadas através do comando <strong>git commit</strong>, tal comando empacota as alterações contidas na stage, com um comentário pelo qual você colocará descrevendo o que foi mudado, esse é o nível final.

<p align="center">
    <img src="./img/local_operations_explanation.png" alt="Imagem Ilustrativa">
 </p>

 ---

 ## Comandos Essenciais 

 ### Git Init

 ```
 git init
 ```
Esse comando é responsável por iniciar a linha do tempo no nosso projeto, criando o diretório git, pelo qual irá registrar todas as configurações relacionadas ao versionamento.

### Git Add

Adciona o arquivos alterados, por exemplo caso eu tenha modificando um "arquivo.txt", e queria colocar ele na Staging Area já explicada anteriormente, basta digitar:
```
git add arquivo.txt
```
Após isso o arquivo selecionado será encaminhado para a <strong>Staging Area</strong>. Caso você queira colocar todos os arquivos alterados em toda a pasta raíz, basta utilizar o comando:
```
git add *
```

### Git Commit

Já citado antes no tópico onde falamos sobre o Git Directory, o comando:
```
git commit -m "exemplo"
```
É utilizado para registrar a alteração de todos os arquivos colocados na <strong>Staging Area</strong> e envia-los para o diretório git, o complemento <strong>-m "exemplo"</strong> é utilizado para destinar uma mensagem pelo qual será usada para identificar em qual ponto na linha do tempo foi alterado e o que foi alterado.

---

# GitHub

Todos os comandos explicados até agora são usados como citado antes em operações locais, em sua máquina pessoal, entre tanto a graça do Git hoje em dia é a utilização de repositórios onlines, e é deles que vamos falar agora, para criar repositórios na nuvem, existem diversas plataformas, como BitBucket, GitLab, entre outros. Porém, o mais popular entre eles e o queridinho dos desenvolvedores, é o GitHub, para utilizar ele é bem fácil, basta acessar esse link, criar sua conta e pronto, você já será capaz de criar repositórios como esse que você está lendo.

## Vinculando GitHub e Git

Agora que já criamos nossa conta no GitHub, vamos configurar algumas coisinhas no github, primeiramente gerar nossa SSH Key, que é a chave pelo qual nos possibilitará entrar em contato com nosso servidor na nuvem do GitHub, para isso existem guias no própio site do GitHub pelos quais eu irei citar aqui: 

- <a href="https://docs.github.com/pt/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent"><strong>Como gerar uma nova chave SSH</strong></a>
- <a href="https://docs.github.com/pt/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account"><strong>Ccomo adcionar sua chave ao GitHub</strong></a>
