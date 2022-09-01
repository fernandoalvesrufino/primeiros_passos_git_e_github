# Bem vindo aos primeiros passos no Git e GitHub

# Índice
- [O que é Git?](#o-que-é-git)
- [O que é GitHub?](#o-que-é-github)
- [O que é um Repositório?](#o-que-é-um-repositório)
- [Instalando o Git no Windows](#instalando-o-git-no-windows)
- [Como criar um repositório?](#como-criar-um-repositório)
- [Como enviar o arquivo para o repositório remoto?](#como-enviar-o-arquivo-para-o-repositório-remoto)

## O que é Git?
![git](https://embarcados.com.br/wp-content/uploads/2015/02/imagem-de-destaque-39.png)

Git é um Sistema de Controle de Versões. Traduzindo... o GIT tem a função de registrar qualquer alteração feita em cima de um código. O Git armazena essas informações (armazena todas as mudanças e alterações feitas no código) e permite que, caso desejar, um(a) programador(a) possa voltar a versões anteriores de uma aplicação de modo simples e rápido. 

## O que é GitHub?
![GitHub](https://miro.medium.com/max/1400/0*ZLfPdBuEy3SgJscw.jpg)

GitHub é uma plataforma de hospedagem e gerenciamento de repositórios. Pode ser de forma privada (onde só nós teremos acesso) ou publica (onde todos que desejarem poderão ter acesso).

## O que é um Repositório?
É um lugar (diretório) onde podemos armazenar, ou colocar, os nossos arquivos e projetos. O Git é o repositório LOCAL, odemos acessar no nosso próprio PC. O GitHub é o repositório REMOTO, podemos acessar em qualquer lugar com acesso à internet.

## Instalando o Git no Windows
Para instalar o Git no Windows, eu recomendo que você siga o passo a passo descrito no site [dicas de programacao](https://dicasdeprogramacao.com.br/como-instalar-o-git-no-windows/). Lá já está tudo detalhado de como fazer.

## Como criar um repositório?
O primeiro passo é INICIAR o repositório. O jeito mais fácil de fazer isso é:
- Depois de instalado o Git no seu PC, crie uma pasta para seus projetos. 
- Em seguida, crie outra pasta com o nome 'projeto_1' e acesse a pasta. 
- Clique com o botão direito do mouse dentro da pasta e selecione a opção Git Bash Here (Ou acesse a pasta através do CMD do Windows). A partir daí, digite o comando:
```
git init
```
Assim um repositório é iniciado. A partir daí, o Git vai reconhecer todas os arquivos dessa pasta como um projeto. Após dado o comando acima é criado um arquivo oculto chamado '.git'

## Adicionando arquivos ao repositório
Podemos fazer isso através da IDE (ambiente de desenvolvimento integrado, o programa usado para escrever os códigos). Podemos abrir a pasta onde iniciamos o repositório (no exemplo dado anteriormente, a pasta chamada 'projeto_1') na nossa IDE. 

Então vamos usar a nossa IDE para criar novos arquivos. Clique com o botão direito do mouse como indicado na imagem abaixo:
![vscode - novo arquivo](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS9A-fLPKa8etiw8WB-aa8BYMCrOfrVOOdh2qvbSrrUTQ&s)

e então, clique em novo arquivo e digite 'nome.txt'
OBS: É necessário colocar o .txt nesse caso (a extensão, ou formato do arquivo). No caso de um arquivo de texto: '.txt', no caso de um código em python '.py', e quando formos criar nosso README '.md' (mais pra frente falamos disso.)
Agora dentro da área à direita (no caso do VSCode) é só digitar algo. Vamos digitar 'Elon Musk'.

Abrindo o CMD (opção TERMINAL > NOVO TERMINAL) digite o comando:
```
git status
```
Esse comando fará com que sejam apresentados todos os arquivos que existem no repositório (no caso 'nomes.txt').

Para que esse arquivo seja monitorado (trackeado) digite o comando:
```
git add nome.txt
\\ git add (nome_do_arquivo.formato)
```
A partir daqui o arquivo está esperando para ser commitado (salvo no repositório). Se eu modificar o arquivo novamente, ao verificar o status ('git status') é indicado que o arquivo foi modificado e que está esperando para ser trackeado (então, seria necessário dar um 'git add nome_do_arquivo.formato' novamente).

Mas caso tenham sido feitas várias criações de arquivos e várias modificações, é possível digitar um comando que fará com que todas as alterações passem a ser monitoradas (trackeadas):
```
git add .
```
Para commitar os arquivos (ou salvar os arquivos no repositório) digitamos o comando:
- Commitar um arquivo único:
```
git commit nome.txt -m "Estou criando um arquivo de nomes"
\\ OBS: Não utilize acentuação na mensagem
```
Note que é possível adicionar uma mensagem após o comando do commit. Essa mensagem é importante para descrever o que foi feito no arquivo editado. Caso tenhamos mais de um arquivo, com esse comando estamos commitando apenas o arquivo 'nome.txt'. Os demais ainda ficariam aguardando para serem commitados. 

- Para commitar todos os arquivos de uma vez utilize o comando:
```
git commit -m "Commitando todos os arquivos de uma vez"
```
## Como enviar o arquivo para o repositório remoto?

Após ter criado uma conta no GitHub, clique no + ao lado da sua foto de perfil no canto superior direito, depois em 'New Repository'. Digite um nome (de preferencia com letras minusculas, sem espaços e sem acentos), role a página para baixo e clique em criar repositório.
