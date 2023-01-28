<div style="display: inline_block"><br>
  <img align="right" alt="Dev-pic" style="border-radius: 50%; width: auto; height:420px;" 
     src="https://business-science.github.io/shiny-production-with-aws-book/img/09_git_cli/git_commands.png">
</div>

<div style="display: inline_block"><br>
  <img align="left" alt="git-command" style="border-radius: 50%; width: auto; height:100px;" 
     src="https://codeguida.com/media/post_title/256px-Git_icon.svg_dMqw0Bl.png">
</div>

# GIT 
Gíria em inglês britânico para cabeça dura
- Sistema de controle de versões
- Criado por **Linus Torvalds** e Junio Hamano
- Lançamento em abril de 2005
- Escrito em C, Shell, Perl

<br>

> ### Configuração
> - git config --global user.name  CARVALHO
> - git config --global user.email marcos.antonio.carvalho@gmail.com
> - git config --list

<br><br><br>

Comando   | Finalidade
--------- | ----------------- 
**git init** *repo-local* | Criar um novo projeto de git. Criar um repositório novo em branco.
**git status** | Mostrar informações de status da branch atual.
**git clone** https://repo-remoto | Baixar uma cópia identica da última versão do repositório no seu computador. 
**git add** *arquivo* ou<br>**git add -A** |  Incluir as alterações de um ou vários arquivos em nosso próximo commit na ***Stage***<br> ou adicionar tudo ao mesmo tempo.
**git commit -m** *"mensagem"* | Salvar nossas alterações no ***Repositório Local***. <br>(talvez após uma tarefa ou resolução de problema específica).
**git push** *repo-remoto branch* <br> **git push -u** *origin branch* | Subir/Upload suas alterações no ***Repositório locall*** para servidor remoto <br> ou todos os arquivos.
**git pull** *repo-remoto*  | Descer/Download as atualizações do repositório remoto e aplica no seu computador (git fetch + git merge).
**git branch** <br> **git branch** *branch* <br> **git branch -d** *branch* | Lista todas as ramificações. <br> Cria um branch com o nome especificado. <br> Deleta o branch com o nome especificado. 
**git checkout** *branch* <br> **git checkout -b** *branch_novo* | Trocar de uma ramificação para outra. <br> cria e faz o checkout de um novo branch.

<div style="display: inline_block"><br>
  <img align="left" alt="git-command" style="border-radius: 50%; width: auto; height:60px;" 
     src="https://nitayneeman.gallerycdn.vsassets.io/extensions/nitayneeman/git-semantic-commit/2.0.0/1581021638044/Microsoft.VisualStudio.Services.Icons.Default">
</div>

## Convenção de mensagem para commit
Substantivo | Finalidade do substantivo da Alteração | Exemplo
:---------- | :------: | -------:
fix      | Correção de bug | fix(scope): bug in scope
feat     | Novo recurso    | feat(parser): add ability to parse arrays <br> feat(api)!: send an email to the customer
build    | Compilação ou dependências externas | 
chore    | Não Afeta codigo fonte fonte ou os testes | chore(deps): update dependencies
ci       | Arquivos e scripts de configuração de CI (Integração Contínua) | 
docs     | Apenas a documentação | docs: update ref docs
style    | Não afetam o significado do código | 
refactor | Não corrige um bug e nem adiciona um recurso | 
perf     | Melhora o desempenho | 
test     | Adicionando testes ausentes ou corrigindo testes existentes | 
revert   | Reverter algo | 
others   | Outras não previstos | 

> **"!"** marca uma alteração de ***última hora*** ou uma alteração muito ***importante*** <br>
> Exemplo: feat! ou feat(api)! 
