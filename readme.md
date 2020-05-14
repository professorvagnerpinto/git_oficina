
Linha adicionada quando estava no ramo master.

Git => é o software que você instala no seu computador para versionar projetos (arquivos);
github | bitbuket | outros => repositório na nuvem onde você armazena o projeto commitado.

Lista com os principais comandos:
$ git status -> exibe o estado da pasta/projeto monitorado
$ git add readme.md -> adiciona um arquivo a árvore do git
$ git add -A -> adiciona todos os arquivos na pasta do prompt a árvore do git
$ git commit -m "Menssagem do commit" -> realiza um commit na pasta do prompt (cria uma versão das alterações realizadas nos arquivos da pasta do prompt)
$ git commit -am "Menssagem do commit" -> também realiza um commit na pasta do prompt, mas agora não depende de um git add -A, isto é, de um git add
$ git log -> exibe o log do (s) commit (s)
$ git branch -> lista todos os ramos do projeto (todos os branchs)
$ git branch nomeDoBranch -> cria um novo ramo (branch)
$ git checkot nomeDoBranch -> muda de branch
$ git reset --soft -> dá um rollback no que foi commitado. Volta para o commit que você determinar e deixa os commits posteriores preparados (prontos para realizar um novo commit.
$ git reset --mixed -> dá um rollback no que foi commitado. Identico ao soft, porém, tem que dar um git add -A novamente ou git commit -am "Mengem de commit"
$ git reset --hard -> dá um rollback no que foi commitado. Simplesmente ignora commits posteriores ao que você determinar. O conteúdo do arquivo some.


Como iniciar, commitar e ver como ficou o projeto/pasta na árvore do git?
1. Na pasta do projeto digite git init, exemplo: 
	vagner@NBdoVagner:~/B7Web/git_oficina$ git init
2. pastaDoProjeto$ git status
3. git add -A
4. git commit -m "Mensagem do commit. Cuida para ser claro no foi realizado"
5. git log

Teorias:
Branch, README e Commit:
	Branch -> ramos do projeto ou versão do projeto, o inicial é o master.
	README (.md) -> local onde geralmente se coloca informações importantes para outra pessoa entender o seu projeto.
	Commit -> salvar as alterações realizadas no projeto. A cada commit cria-se uma nova verão das modificações realizadas no projeto.
