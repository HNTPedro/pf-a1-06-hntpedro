# A1.06 PrettyFlights - Fluxo de Trabalho pela Estratégia GitFlow

## 1. Configuração e Inicialização

**"git config"**: Define as credenciais de usuário (nome e e-mail).
`git config --global user.name "Seu Nome"`
`git config --global user.email "seu@email.com"`

**git init**: Transforma uma pasta comum em um repositório Git local.
`git init`
`git init meu-projeto-novo`

**git clone**: Baixa um projeto existente do GitHub para o seu PC.
`git clone https://github.com/usuario/projeto.git`
`git clone git@github.com:usuario/projeto.git`

## 2. Ciclo de Alterações

**git add**: Adiciona arquivos à área de preparação (staging).
`git add index.html`
`git add .` (adiciona tudo)

**git commit**: Cria um "ponto de salvamento" com uma mensagem descritiva.
`git commit -m "Cria cabeçalho do site"`
`git commit --amend` (edita o último commit)

**git status**: Mostra o estado atual dos arquivos (modificados, rastreados, etc.).
`git status`
`git status -s` (versão resumida)

**echo**: Cria e exibe textos dentro de arquivos
`echo "texto" > arquivo.txt` 
cria um arquivo chamado arquivo.txt com o conteúdo "texto". Se o arquivo já existir, ele será apagado e substituído.
`echo "conteúdo" >> arquivo.txt` adiciona uma nova linha com "conteúdo" ao final do arquivo


## 3. Sincronização com o GitHub

**git remote**: Gerencia a conexão entre o repositório local e o remoto.
`git remote add origin https://github.com/user/repo.git`
`git remote -v` (lista conexões)

**git push**: Envia seus commits locais para o GitHub.
`git push origin main`
`git push -u origin feature-nova`

**git pull**: Baixa as novidades do GitHub e já as mescla no seu código.
`git pull origin main`
`git pull --rebase`

**git fetch**: Baixa o histórico do servidor sem alterar seus arquivos locais.
`git fetch origin`
`git fetch --all`

## 4. Ramificação (Branches)

**git branch**: Gerencia as ramificações.
`git branch` (lista todas)
`git branch -d nome-da-branch` (deleta)

**git checkout / switch**: Troca de uma branch para outra.
`git checkout -b nova-feature` (cria e muda)
`git switch main`

**git merge**: Une o trabalho de uma branch em outra.
`git merge feature-concluida`
`git merge --no-ff dev`

**git stash**: Guarda alterações temporariamente para limpar o diretório sem fazer commit.
`git stash` (esconde)
`git stash pop` (recupera)

## 5. Inspeção e Log

**git log**: Lista o histórico de commits.
`git log --oneline` (resumo de uma linha)
`git log -p -2` (mostra as mudanças dos últimos 2 commits)

**git show**: Mostra detalhes de um objeto específico (commit, tag).
`git show abc1234`
`git show HEAD`

**git blame**: Mostra quem alterou cada linha de um arquivo e quando.
`git blame script.js`
`git blame -L 10,20 arquivo.txt` (linhas 10 a 20)

## 6. Desfazendo Erros

**git reset**: Desfaz commits ou tira arquivos do staging.
`git reset --soft HEAD~1` (volta 1 commit, mantém o código)
`git reset --hard origin/main` (reseta tudo para o estado do servidor)

**git revert**: Cria um novo commit que desfaz as alterações de um commit anterior (seguro para projetos públicos).
`git revert abc1234`
`git revert HEAD`
