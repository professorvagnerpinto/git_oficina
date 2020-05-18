<h1>Ofinina de Git e github</h1>

<h4>Referências</h4>
    <ol>
        <li>Material baseado em B7Web - módulo7 #1 ao #7 - Git Versionamento de código</li>
        <li>Como estilizar arquivos .md (markdown): https://medium.com/@raullesteves/github-como-fazer-um-readme-md-bonit%C3%A3o-c85c8f154f8</li>
        <li>Template de arquivo .md (inglês, português e espanhol): https://github.com/dbader/readme-template</li>
    </ol>

<h2>Teorias</h2>
    <p>Git => é o software que você instala no seu computador para versionar projetos (arquivos).</p>
    <p>github | bitbuket | outros => repositório na nuvem onde você armazena o projeto commitado e compartilha com outros desenvolvedores (equipe). É 	possível ter versões locais diferentes das remotas e vice-versa. É possível sincronizar o Git local com o remoto, e vice-versa.</p>
    <p>Branch, README e Commit:</p>
    <ul>
        <li>Branch -> ramos do projeto ou versão do projeto, o inicial é o master.</li>
    	<li>README (.md - markdown) -> local onde geralmente se coloca informações importantes para outras pessoas entender o seu projeto.</li>
    	<li>Commit -> salvar as alterações realizadas no projeto. A cada commit cria-se uma nova verão das modificações realizadas no projeto.</li>
    </ul>

<h2>Git local</h2>
    <p>Como iniciar, commitar e ver como ficou o projeto/pasta na árvore do git?</p>
    <ol>
        <li>Na pasta do projeto digite git init, exemplo (isso inicializa o git local na pasta do prompt): vagner@NBdoVagner:~/B7Web/git_oficina$ git init</li>
        <li>pastaDoProjeto$ git status (isso indica o estado do repositório)</li>
        <li>git add -A (isso adiciona todos os arquivos no tracker do git, isto é, eles ficam observáveis pelo git)</li>
        <li>git commit -m "Mensagem do commit. Cuida para ser claro no foi realizado" (commita, isto é, registra todas as alterações na árvore do git)</li>
        <li>git log (para ver o commit no log do git)</li>
    </ol>

<h4>Lista com os principais comandos (git local):</h4>
    <ul>
        <li>$ git init -> para inicializar o monitoramento do git em uma pasta (escolha a pasta raiz do projeto, assim monitora todo projeto)</li>
        <li>$ git status -> exibe o estado da pasta/projeto monitorado</li>
        <li>$ git add readme.md -> adiciona um arquivo a árvore do git</li>
        <li>$ git add -A -> adiciona todos os arquivos na pasta do prompt a árvore do git</li>
        <li>$ git commit -m "Menssagem do commit" -> realiza um commit na pasta do prompt (cria uma versão das alterações realizadas nos arquivos da pasta do prompt)</li>
        <li>$ git commit -am "Menssagem do commit" -> também realiza um commit na pasta do prompt, mas agora não depende de um git add -A, isto é, de um git add</li>
        <li>$ git log -> exibe o log do (s) commit (s)</li>
        <li>$ git branch -> lista todos os ramos do projeto (todos os branchs)</li>
        <li>$ git branch nomeDoBranch -> cria um novo ramo (branch)</li>
        <li>$ git branch -D nomeDoBranch -> deleta um branch (para isso você deve estar em um branch diferente do branch a excluir)</li>
        <li>$ git checkout nomeDoBranch -> muda de branch</li>
        <li>$ git diff -> para exibir os arquivos e as alterações realizadas no ramo atual</li>
        <li>$ git diff --name-only -> exibe só os nomes dos arquivos que sofreram alteração</li>
        <li>$ git diff nome_do_arquivo -> para identificar as alterações realizadas em um arquivo em específico</li>
        <li>$ git checkout HEAD -- nomeDoArquivo -> para retirar o arquivo da lista de observáveis do Git (use diff para ver quais são antes)</li>
        <li>$ git reset --soft -> dá um rollback no que foi commitado. Volta para o commit que você determinar e deixa os commits posteriores preparados (prontos para realizar um novo commit.</li>
        <li>$ git reset --mixed -> dá um rollback no que foi commitado. Identico ao soft, porém, tem que dar um git add -A novamente ou git commit -am "Mengem de commit"</li>
        <li>$ git reset --hard -> dá um rollback no que foi commitado. Simplesmente ignora commits posteriores ao que você determinar. O conteúdo do arquivo some.</li>
        <li>$ git revert --no-edit token_do_commit -> dá um rollback no que foi commitado, mas deixa o conteúdo no estado que se encontrava. Esse é o "salvador da sexta-feira", pois, conta o dito popular, que se crachar a aplicação no final de semana, e o problema foi do último commit, é só você dar um git revert para voltar ao que estava funcionando anteriormente, aí na segunda você descobre o problema de seu commit da sexta-feira. Ah! o --no-edit é para evitar que o Git abra o editor que você cadastrou para o projeto. E o token_do_commit é o id do commit que você deve pegar no git log.</li>
    </ul>

<h2>Git remoto</h2>
    <h4>Como fazer upload do seu repositório?</h4>
        <ol>
            <li>Execute $ git remote add origin https://github.com/seu_usuario/seu_repositório.git (na primeira vez que você fizer upload)</li>
            <li>Execute $ git push -u origin master (nesse exemplo, para enviar o branch master (local) para o branch origin (remoto) )</li>
            <li>Digite os dados solicitados, usuário e senha (do seu repositório no github ou outro de sua preferência)</li>
        </ol>
    <h4>Lista com os principais comandos (git remoto):</h4>
            <ul>
                <li>$ git remote add origin https://github.com/seu_usuario/seu_repositório.git -> adicionar o repositório remoto ao git local</li>
                <li>$ git push -u origin master -> fazer o upload do repositório local -> sintaxe: comando enviar flag destino_no_remote branch_a_enviar</li>
                <li>$ git remote -> para saber se o repositório local foi adicionado ao remoto (o upload aconteceu)</li>
                <li>$ git remote -v -> para exibir mais detalhes do que foi adicionado ao repositório remoto</li>
                <li>$ git remote fetch -> para baixar as atualizações do repositório remoto para o local</li>
                <li>$ git remote push -> para enviar as atualizações do repositório local para o remoto</li>
                <li>$ git push origin :nome_do_branch -> remove um branch remoto (atente para os dois pontos antes do nome do branch)</li>
                <li>$ git pull origin nome_do_branch -> puxa as alterações de outros devs do repositório remoto</li>
                <li>$ git clone url_do_projeto_a_clonar -> cria uma cópia do repositório remoto na pasta onde está o prompt</li>
            </ul>
        <p>++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++</p>
         <p>
             Dica!!!
             <br></br>
              Antes de dar um push dê um pull. Isso evita conflitos, pois você terá no seu branch local todas as últimas alterações que outros
              devs fizeram no branch remoto.
         </p>
        <p>++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++</p>
        
<h2>fork (contribuindo com projetos de outros devs no github)</h2>
    <ol>
        <li>Botão fork no dash do github, vai criar um repositório identico ao repositório do projeto original na sua conta do github, assim você passa a contribuir com o projeto original a partir desse clone.</li>
        <li>Faça do clone do projeto criado pelo fork no seu repositório, isto é, o fork criou um clone para você na sua conta do github e agora você vai baixar esse clone para o seu computador, para o seu repositório local. É o clone do clone.</li>
        <li>Faça as alterações que você deseja fazer para contribuir com o projeto original, faça o commit e o push, e no github abra um pull request.</li>
    </ol>

<h2>.gitIgnore</h2>
    <p>
    Importante configuração do projeto. Isso reduz a visibilidade de arquivos sensíveis no repositório remoto. Coisas como chaves de acesso, tokens, entre outros devem ser protegidos pelo desenvolvedor e não podem ter visibilidade no repositório remoto.
    Acesse: https://github.com/github/gitignore para ter uma visão geral dos arquivos ignorados nos principais projetos do github.
    </p>
