Untracked -> Arquivo acabou de ser adicionado mas ainda não foi visto pelo git

Unmodified -> Depois de adionar o arquivo ela passa a ser unmodified, ele existe no git mas não foi modificado

Modified -> Arquivo modificado

Staged -> Momento em que o arquivo fica marcado para ir para próxima versão.

Depois de commitado, todos os arquivos que estão marcados como staged são levados para uma nova versão e marcados com unmodified

Commit - Momento em que é criado um snapshoot uma imagem dos arquivos

git commit -m "Observação, coloque informações relevantes no commit, dizendo o que foi feito como correções de bug,novas funcionalidade e etc...";


LOG

git log 
git shorlog
git log --author="name"
git log --graph /*Mostra graficamente os merges*/

//Informações do commit
git show hashDoCommit

/*Revisar quais alterações foram feitas*/
git diff
git diff --name-only


git commit -am "message"

-a:stage files que foram modificados ou removidos, mas arquivos novos que não foram adicionados não são afetados

FIZ BESTEIRA E AGORA

/*Retira as mudanças feitas nos arquivos*/
git checkout nomeArquivo
/*Retirar do stage, volta para o ponteiro que ja estou*/
git reset HEAD nomeArquivo

