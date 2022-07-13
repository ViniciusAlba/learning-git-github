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
