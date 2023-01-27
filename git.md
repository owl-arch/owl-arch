<div style="display: inline_block"><br>
  <img align="right" alt="Dev-pic" style="border-radius: 50%; width: auto; height:420px;" 
     src="https://business-science.github.io/shiny-production-with-aws-book/img/09_git_cli/git_commands.png">
</div>

### GIT (gíria em inglês britânico para cabeça dura) 
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


