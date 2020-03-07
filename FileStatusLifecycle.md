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

git reset --soft   hash do anterior
git reset --mixed hash do anterior
git reset --hard hash do anterior


Já subi as alterações para o repositório o que fazer?
Você pode usar o git reset --hard <hash_do_commit_anterior> e depois forçar a subida com git push origin master --force

## Branch
### O que é?
É um ponteiro móvel que leva um commit

### Porque usar?

* Poder modificarsem alterar o local principal (master)
* Facilmente "desligável"
* Múltiplas pessoas trabalhando
* Evita conflitos
### Como usar?
git checkout -b  nomeBranch
git branch --em qual branch estou 
git checkout nomeBranch --muda de branch
git branch -D nomeBranch -- apagando branch

### Unindo Branches

- Merge
Vantagens
* Operação não destrutiva

Contra
* Commit extra, que não faz nada só junta coisas.
* Histórico poluído.

- Rebase
Vantagens
* Evita commits extras
* Histórico linear
Contra
* Perde ordem cronológica

###  Como unilos
git merge NomeBranch

git rebase NomeBranch

## Extras
Estou com uma trabalho é quero mudar para outra branch mas não quero levar as alterações
comigo para nova branch o que fazer

git stash
git stash apply -- para retornar com as modificações

## .gitignore 
-- Arquivo utilizado para deixar untracked os arquivos que você não que subir ou manter snapshoots

### Alias

git config --global alias.atalhoname o que o comando faz
EX: git config --global alias.s status;

### Salvando sua sexta-feira
--Retorna as modificações do commit, mas sem peder o trabalho feito
git revert hashgit
