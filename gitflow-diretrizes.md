## GitFlow - PrettyFlights
Foi utilizado o comando 'git checkout -b develop' para criar uma nova branch permanente para realizar o desenvolvimento
Foi utilizado o comando 'git push -u origin develop' para enviar o comit
Foi utilizado o comando 'git checkout -b feature/leitura-qrcode develop' para criar uma nova branch temporaria para desenvolver a feature
Foi criado o arquivo .js para dar inicio ao código da feature
O arquivo do código é adcionado e comitado logo em seguida
É utilizado o 'git checkout develop' para voltar a branch do develop, e usado o 'git merge --no-ff feature/leitura-qrcode' para mesclar o desenvolvimento feito no 'feature' para o 'develop'
As mudanças são realizadas com o 'git push origin develop'
É usado 'git branch -d feature/leitura-qrcode' para apagar a branch original
'git checkout -b release/1.0.0 develop
git checkout main
git merge --no-ff release/1.0.0
git tag -a v1.0.0 -m "Versão 1.0.0 oficial"
git push origin main --tags

git checkout develop
git merge --no-ff release/1.0.0
git push origin develop
git branch -d release/1.0.0
'
A branch de release é criado e é mesclada ao main, então o 'develop' é atualizado e a branch de release é excluida
