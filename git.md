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


<br>

## Convenção de mensagem para commit

#### A mensagem do commit deve ser estruturada da seguinte forma:
> **tipo/substantivo**(escopo opcional): descrição <br><br>
> [corpo opcional] <br><br>
> [rodapé(s) opcional(is)]
<br>

Substantivo | Finalidade do substantivo da Alteração | Exemplo
:---------- | :------: | -------:
fix      | Correção de bug | fix(scope): bug in scope
feat     | Novo recurso    | feat(parser): add ability to parse arrays <br> feat(api)!: send an email to the customer
build    | Compilação ou dependências externas | build: update dependencies
chore    | Não Afeta codigo fonte fonte ou os testes | chore(deps): update dependencies
ci       | Arquivos e scripts de configuração de CI (Integração Contínua) | 
ops      | Componentes operacionais como infra, implantação, backup, ... |
docs     | Apenas a documentação | docs: update ref docs
style    | Não afetam o significado do código | style: remove empty line
refactor | Não corrige um bug e nem adiciona um recurso | refactor: implement calculation method as recursion
perf     | Melhora o desempenho | 
test     | Adicionando testes ausentes ou corrigindo testes existentes | 
revert   | Reverter algo | 
others   | Outras não previstos | 

<br>

> Um commit que contém no rodapé opcional o texto **BREAKING CHANGE:**, ou contém o **símbolo ! depois do tipo/escopo**, introduz uma modificação que **quebra a compatibilidade da API** (isso se correlaciona com MAJOR do versionamento semântico). <br>
> Uma BREAKING CHANGE pode fazer parte de commits de qualquer tipo


<br>

## Normatização (Especificação) da Conventional Commits
<https://www.conventionalcommits.org/pt-br/v1.0.0/>
> As palavras-chaves “DEVE” (“MUST”), “NÃO DEVE” (“MUST NOT”), “OBRIGATÓRIO” (“REQUIRED”), “DEVERÁ” (“SHALL”), “NÃO DEVERÁ” (“SHALL NOT”), “PODEM” (“SHOULD”), “NÃO PODEM” (“SHOULD NOT”), “RECOMENDADO” (“RECOMMENDED”), “PODE” (“MAY”) e “OPCIONAL” (“OPTIONAL”), nesse documento, devem ser interpretados como descrito na **RFC 2119**.

1. A mensagem de commit DEVE ser prefixado com um tipo, que consiste em um substantivo, feat, fix, etc., seguido por um escopo OPCIONAL, símbolo OPCIONAL !, e OBRIGATÓRIO terminar com dois-pontos e um espaço.

1. O tipo feat DEVE ser usado quando um commit adiciona um novo recurso ao seu aplicativo ou biblioteca.

1. O tipo fix DEVE ser usado quando um commit representa a correção de um problema em seu aplicativo ou biblioteca.

1. Um escopo PODE ser fornecido após um tipo. Um escopo DEVE consistir em um substantivo que descreve uma seção da base de código entre parênteses, por exemplo, fix(parser): .

1. Uma descrição DEVE existir depois do espaço após o prefixo tipo/escopo. A descrição é um breve resumo das alterações de código, por exemplo, fix: problema na interpretação do array quando uma string tem vários espaços.

1. Um corpo de mensagem de commit mais longo PODE ser fornecido após a descrição curta, fornecendo informações contextuais adicionais sobre as alterações no código. O corpo DEVE começar depois de uma linha em branco após a descrição.

1. Um corpo de mensagem de commit é livre e PODE consistir em infinitos parágrafos separados por uma nova linha.

1. PODE(M) ser fornecidos um ou mais rodapés, uma linha em branco após o corpo. Cada rodapé DEVE consistir em um token de palavra, seguido por um separador :<espaço> ou <espaço>#, seguido por um valor de uma string (isso é inspirado pelo git trailer convention).

1. Um token de rodapé DEVE usar - no lugar de espaços em branco, por exemplo, Acked-by (isso ajuda a diferenciar a seção de rodapé de um corpo de vários parágrafos). Uma exceção é feita para BREAKING CHANGE, que PODE também ser usado como um token.

1. O valor de um rodapé PODE conter espaços e novas linhas, e a análise (parsing) DEVE terminar quando o próximo token/separador de rodapé válido for encontrado.

1. BREAKING CHANGES DEVEM ser indicadas após o tipo/escopo de uma mensagem de commit, ou como uma entrada no rodapé.

1. Se incluída como um rodapé, uma alteração de quebra DEVE consistir no texto em maiúsculas QUEBRAR ALTERAÇÃO, seguido por dois pontos, espaço e descrição, por exemplo, BREAKING CHANGE: as variáveis de ambiente agora têm precedência sobre os arquivos de configuração.

1. Se incluído no prefixo de tipo/escopo, as BREAKING CHANGES DEVEM ser indicadas por um ! imediatamente antes de :. Se o símbolo ! for usado, BREAKING CHANGE: PODE ser omitido da seção de rodapé, e a descrição da mensagem de commit DEVE ser usada para descrever a BREAKING CHANGE.

1. Tipos diferentes de feat e fix PODEM ser usados em suas mensagens de commit, por exemplo, docs: documentos de referência atualizados

1. As unidades de informação que compõem o Conventional Commits NÃO DEVEM ser tratadas com distinção entre maiúsculas e minúsculas pelos implementadores, com exceção de BREAKING CHANGE que DEVE ser maiúscula.

1. BREAKING-CHANGE DEVE ser sinônimo de BREAKING CHANGE, quando usado como um token em um rodapé.

### Porque utilizar Conventional Commits
- Criação automatizada de CHANGELOGs.
- Determinar automaticamente alterações no versionamento semântico (com base nos tipos de commits).
- Comunicar a natureza das mudanças para colegas de equipe, o público e outras partes interessadas.
- Disparar processos de build e deploy.
- Facilitar a contribuição de outras pessoas em seus projetos, permitindo que eles explorem um histórico de commits melhor estruturado.
