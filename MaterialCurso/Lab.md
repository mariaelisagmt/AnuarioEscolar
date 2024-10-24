## Laboratório: Trabalhando com Git

**Objetivo:** Familiarizar-se com os comandos básicos do Git através de um
 exercício prático.
 
**Passos:**

 1. Crie um novo diretório em seu computador e navegue até ele no terminal.
 2. Inicialize um novo repositório Git com git init.
 3. Crie um novo arquivo chamado index.html e adicione o seguinte conteúdo:
```html
 <!DOCTYPE html>
 <html>
 	<head>
 		<title>Git Branch</title>
 		<style>
 			body {
 				background-color: #ffcc00;
 				display: flex;
 				justify-content: center;
				align-items: center;
				height: 100vh;
				font-family: Arial, sans-serif;
 				}
 		</style>
 	</head>
 	<body>
 	<h1>Hello, Git master branch!</h1>
 	</body>
 </html>
```
 4. Use git add para adicionar index.html ao índice do Git.
 5. Faça um commit das alterações com git commit-m "Adicionado
 index.html".
 6. Verifique o status do seu repositório com git status. Você deve ver que
 não há alterações a serem commitadas.
 7. Crie uma nova branch com git branch nova_branch.
 8. Mude para a nova branch com git checkout nova_branch.
 9. Modifique o arquivo index.html para dizer “Hello, new branch!” no elemento `<h1>`.
 10. Adicione e faça commit das alterações com git add e git commit.
 11. Mude de volta para a branch principal com git checkout master.
 12. Faça merge da nova_branch na branch principal com git merge
 nova_branch.
 13. Verifique o conteúdo de index.html. Deve dizer “Hello, nova branch!” no
 elemento `<h1>`.

## Laboratório Avançado: Gerenciando Ambientes com Git e HTML
**Objetivo:** Aprender a gerenciar diferentes ambientes de desenvolvimento usando
 branches no Git e alterando a cor de fundo de uma página HTML de acordo
 com a branch.
 
**Passos:**
 1. No mesmo repositório criado anteriormente, crie uma nova branch para
 cada ambiente com git branch DEV, git branch STAGE e git branch
 PROD.
 2. Mude para a branch DEV com git checkout DEV.
 3. Modifique o arquivo index.html para alterar a cor de fundo para azul (por
 exemplo, altere a linha com background-color para background-color:
` #0000ff`.
 4. Adicione e faça commit das alterações com git add e git commit.
 5. Repita os passos 2 a 4 para a branch STAGE, alterando a cor de fundo
 para verde (background-color: `#00ff00`;).
 6. Repita os passos 2 a 4 para a branch PROD, alterando a cor de fundo para
 vermelho (background-color: `#ff0000`;).
 7. Agora, suponha que você tenha uma alteração que precisa ser replicada
 em todos os ambientes. Volte para a branch master com git checkout
 master.
 8. Faça a alteração necessária no arquivo index.html (por exemplo, adicione
 um novo parágrafo `<p>Hello, all branches!</p>`).
 9. Adicione e faça commit das alterações com git add e git commit.
 10. Mude para a branch DEV com git checkout DEV e faça merge da branch
 master com git merge master.
 11. Repita o passo 10 para as branches STAGE e PROD.
 12. Verifique o conteúdo de index.html em cada branch. Deve conter a
 alteração comum além da cor de fundo específica de cada ambiente.
