### Clonar repositório
git clone <caminho> <nome>
Ex.:


- criar novo branch local

$ git branch iss53

- mudar de branch

$ git checkout iss53

- criar novo branch local e ja acessá-lo

$ git checkout -b iss53

- empurrar branch local para servidor (repositório remoto)

git push <remote> <branch>
Ex
$ git push origin serverfix
Ou
$ git push origin serverfix:serverfix

- criar novo branch (e acessá-lo) com ligação já feita com sua versão remota ja existente

git checkout -b [branch] [remotename]/[branch]
Ex
$ git checkout -b serverfix origin/serverfix

- para fazer com que uma branch local passe a rastrear uma branch remota

$ git checkout --track origin/serverfix

- mesclar branches

$ git checkout master (primeiro acessar a branch que vai receber a mescla)
$ git merge hotfix (fazer a mescla especificando de que branch vêm as alterações)

- ver branches locais com mais informações, incluindo o que cada filial está rastreando e se sua filial local está à frente, atrás ou ambos

$ git fetch --all (para buscar info atualizada do servidor)
$ git branch -vv

- para apagar uma branch remota (depois que ela ja foi mesclada localmente no master e o master empurrado pro servidor)
git push <remote> --delete <branch>
$ git push origin --delete serverfix

