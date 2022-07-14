# Git e Github

## Comandos interessantes:
- mkdir -> Cria um novo diretório;
- cd -> Altera entre diretórios;
- git init -> Inicia um novo repositório;
- vi nomeArquivo -> Cria um novo arquivo;
- i -> Edita o novo arquivo;
- esc e depois :wq -> Salva e sai do novo arquivo;
- touch nomeArquivo -> Também cria um arquivo;
- code . -> Abre o diretório, arquivo no VSCode;
- git add -> Adiciona arquivos e diretórios para commitar;
- git commit -m "mensagem" -> Commita novas mundanças;
- git status -> Visualiza o ciclo dos status dos arquivos;
- git log -> Mostra a hash do commit, o autor, a data e a mensagem de commit;
- git log --decorate -> Mostra de qual branch para qual branch foi, se houve merge, quais tags foram geradas, etc;
- git log --author="nome" -> Lista todos os commits com o autor;
- git shortlog -> Mostra em ordem alfabética quais foram os autores, quais commits fizeram e quantos foram;
- git shortlog -sn -> Mostra quantidade de commits e o nome da pesso que commitou;
- git log --graph -> Mostra em forma gráfica o que está acontecendo com as branchs e versões;
- git show hashDoCommit -> Mostra o que foi adicionado ou removido, detalhe por detalhe;
- git diff -> Mostra as últimas coisas que foram feitas, é importante usar antes de commitar;
- git diff --name-only -> Mostra somente o nome do arquivo que foi modificado;
- git checkout nomeArquivo -> Retorna o arquivo para antes da edição (Isso fora do stage);
- git reset HEAD nomeArquivo -> Remove do stage o arquivo do local que estamos. Tiramos da fila do stage;
- git reset --soft nomeArquivo -> Não toca no arquivo de índice ou na árvore de trabalho (mas redefine o cabeçalho para <commit>, assim como todos os modos fazem). Isso deixa todos os seus arquivos alterados como "Changes to be committe" (Alterações onde serão realizados os commits), como o git status colocaria.
- git reset --mixed nomeArquivo -> Redefine o índice, mas não a árvore de trabalho (ou seja, os arquivos alterados são preservados, mas não marcados para um commit) e relata o que não foi atualizado. Esta é a ação predefinida.
- git reset --hard nomeArquivo -> Redefine o índice e a árvore de trabalho. Quaisquer alterações nos arquivos rastreados na árvore de trabalho desde <commit> serão descartados.
- git clone -> Permite clonar todo um repositório para a sua máquina local.
- git checkout -b nomeBranch -> Cria uma nova branch e já entra.
- git branch -> Mostra as branches existentes e em qual estamos.
- git checkout nomeBranch -> Muda para a branch em que colocamos o nome.
- git branch -D nomeBranch -> Deletamos uma branch.

## O QUE É BRANCH?
É um ponteiro móvel que leva a um commit.
O primeiro branch que sempre teremos quando iniciamos um repositório chama-se "Master".
Cada vez que fazemos um commit, o branch vai seguindo os commits. Mas podemos criar um outro branch que pode apontar para o mesmo commit, ou um outro branch apontando para um outro commit.

## POR QUE USAR ESSA FORMA DE BRANCHES?
- Poder modificar os arquivos sem alterar o local principal (master ou main);
- Facilmente "desligável" (Podendo criar e apagar branchs com muita facilidade);
- Múltiplas pessoas trabalhando em diferentes branchs sem um atrapalhar o outro;
- Evita conflitos (Em um único branch com muitas pessoas trabalhando, eu poderia commitar e mais 100 pessoas commitarem ao mesmo tempo, isso seria ruim por conta do tempo. Teriamos que realinhar os commits no histórico e subir sem ter conflito nenhum).

## UTILIZANDO MERGE E REBASE PARA UNIR BRANCHES
Os dois fazem basicamente a mesma coisa, unir as branches. São feitas de formas bem diferentes.

### MERGE
Sempre que utilizarmos um merge, ele vai criar um commit extra juntando a branch separada com as modificações da branch que estamos jogando.

#### PRO
- Operações não destrutiva (não destrói nenhum commit, vai criar um novo para juntar tudo. Não movimentando histórico);

#### CONTRA
- Commit extra (commit que não faz nada, não junta código, não cria arquivo novo, somente une);
- Histório poluído (com a forma diamante, isso fica um pouco complicado para ler se tivermos várias branches);

