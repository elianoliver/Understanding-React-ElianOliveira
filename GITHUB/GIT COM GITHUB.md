## Sumário
- [[#Verificando se o Git está instalado]]
- [[#Configurando o usuário e o e-mail]]
- [[#Iniciando um repositório local]]
	- [[#Criando um arquivo]]
	- [[#Adicionando alterações ao repositório]]
	- [[#Commitando as alterações]]
- [[#Iniciando um repositório Remoto]]
	- [[#Passo 1 Crie um novo repositório]]
	- [[#Passo 2a Inicialize um novo repositório e envie seu código]]
	- [[#Passo 2b Push de um Repositório Local Existente para o GitHub]]
	- [[#Passo 2c Clonando um Repositório Remoto com Git]]
	- [[#Passo 3 Envie seu código para o repositório remoto]]
## Verificando se o Git está instalado
Para verificar se o Git está instalado no seu computador, abra um terminal e execute o comando:
```
git --version
```

Se o Git estiver instalado, você verá uma saída semelhante a esta:
```
git version 2.33.1
```

## Configurando o usuário e o e-mail
O Git precisa saber seu nome de usuário e endereço de e-mail para rastrear suas alterações e enviar solicitações de pull para o GitHub. Para configurar essas informações, execute o comando:
```
git config --global user.name "Seu nome de usuário"
git config --global user.email "Seu endereço de e-mail"
```
ou
```shel
git config --local user.email you@example.com
git config --local user.name "Your Name"
``` 
 
Substitua "Seu nome de usuário" e "Seu endereço de e-mail" pelos seus dados reais.

#### Visualize as configurações do projeto usado
Para ver o email e usuário utilizados no git sendo usados no momento, utilize o seguinte comando:
```shell
git config user.name
git config user.email
```

## Iniciando um repositório local
Para iniciar um repositório local, crie um novo diretório e entre nele:
```
mkdir meu-projeto
cd meu-projeto
```

Em seguida, execute o comando:
```
git init
```

Este comando criará um arquivo `.git` no diretório atual, que armazenará as informações sobre o repositório.

#### Criando um arquivo
Agora que criamos um repositório local, podemos começar a criar arquivos. Crie um novo arquivo chamado `README.md` e adicione o seguinte conteúdo:
```
# Meu projeto

Este é um projeto de exemplo para aprender a usar o Git com o GitHub.
```

Salve o arquivo.

#### Adicionando alterações ao repositório
Para adicionar as alterações ao repositório, execute o comando:
```
git add README.md //para adicionar apenas esse arquivo
```
ou
```shell
git add . //para adicionar todos os arquivos da pasta
```
Este comando adicionará o arquivo `README.md` à lista de alterações que serão commitadas.

#### Commitando as alterações
Para commitar as alterações, execute o comando:
```
git commit -m "Adicionando o README"
```

Este comando criará um novo commit com as alterações que você adicionou.

## Iniciando um repositório Remoto
Neste tutorial, vou explicar passo a passo como criar um repositório remoto no GitHub, uma plataforma popular para hospedar projetos de código-fonte.
#### Passo 1: Crie um novo repositório
1. No canto superior direito da página inicial do GitHub, clique no ícone "+", e no menu suspenso, selecione "New repository".

2. Você será direcionado para a página de criação de um novo repositório. Preencha as informações necessárias:

   - **Repository name**: Escolha um nome único para o seu repositório.
   - **Description** (opcional): Adicione uma breve descrição do seu projeto.
   - **Visibility**: Você pode escolher entre "Public" (público) ou "Private" (privado), dependendo das suas necessidades.
   - **Initialize this repository with**: Você pode escolher adicionar um arquivo README, um arquivo .gitignore e/ou uma licença ao seu repositório, se desejar.

3. Após preencher as informações, clique no botão "Create repository".

#### Passo 2a: Inicialize um novo repositório e envie seu código
Agora que você criou um repositório no GitHub, siga estas etapas para inicializar seu repositório local e enviar seu código para o repositório remoto:

1. Abra o terminal no seu computador.

2. Navegue até a pasta do seu projeto usando o comando `cd`:
   ```shell
   cd /caminho/para/seu/projeto
   ```

3. Inicialize um repositório Git local com o comando `git init`:
   ```shell
   git init
   ```

4. Crie um arquivo README.md (ou outro nome de arquivo de sua escolha) usando um editor de texto ou o comando `echo`:
   ```shell
   echo "# Meu Projeto" >> README.md
   ```

5. Adicione o arquivo README.md ao controle de versão com o comando `git add`:
   ```shell
   git add README.md
   ```

6. Faça o primeiro commit para o seu repositório com o comando `git commit`:
   ```shell
   git commit -m "Primeiro commit"
   ```

7. Configure a branch principal para "main" (ou outro nome de sua escolha) com o comando `git branch`:
   ```shell
   git branch -M main
   ```

8. Adicione o repositório remoto do GitHub como origin com o comando `git remote`:
   ```shell
   git remote add origin https://github.com/seu-usuario/seu-repositorio.git
   ```

Certifique-se de substituir a URL pelo URL do repositório que você criou no GitHub.

9. Envie seu código para o repositório remoto com o comando `git push`. Certifique-se de usar a mesma branch que você configurou anteriormente (no exemplo, "main"):
   ```shell
   git push -u origin main
   ```

Isso enviará seu código para o repositório remoto no GitHub.

E é isso! Você agora criou um novo repositório no GitHub e enviou seu código para ele usando o terminal. Seu projeto está pronto para ser compartilhado e colaborado com outros desenvolvedores.

#### Passo 2b: Push de um Repositório Local Existente para o GitHub
Se você já tem um repositório Git local e deseja enviá-lo para o GitHub, siga estas etapas:

1. Abra o terminal no seu computador.

2. Navegue até a pasta do seu projeto usando o comando `cd`:
   ```shell
   cd /caminho/para/seu/projeto
   ```

3. Associe seu repositório local a um repositório remoto no GitHub usando o comando `git remote`:
   ```shell
   git remote add origin https://github.com/seu-usuario/seu-repositorio.git
   ```

Certifique-se de substituir a URL pelo URL do repositório que você deseja associar.

4. Configure a branch principal para "main" (ou outro nome de sua escolha) usando o comando `git branch`:
   ```shell
   git branch -M main
   ```

5. Envie seu código para o repositório remoto no GitHub com o comando `git push`. Certifique-se de usar a mesma branch que você configurou anteriormente (no exemplo, "main"):
   ```shell
   git push -u origin main
   ```

Isso enviará seu repositório local existente para o repositório remoto no GitHub. Agora seu projeto está hospedado no GitHub e pode ser acessado e colaborado por outros desenvolvedores.

Claro, aqui está um tutorial em Markdown sobre como usar o comando `git clone` para puxar um repositório remoto e começar a trabalhar nele:

#### Passo 2c: Clonando um Repositório Remoto com Git
Clonar um repositório remoto é a maneira mais simples de começar a trabalhar em um projeto existente no GitHub. Siga estas etapas para clonar um repositório para o seu computador:

1. Copie a URL do Repositório
Primeiro, você precisa obter a URL do repositório remoto que deseja clonar. Você pode encontrar a URL no GitHub, na página do repositório. Por exemplo, a URL terá um formato como este: `https://github.com/seu-usuario/seu-repositorio.git`.

2. Abra o terminal
Abra o terminal ou prompt de comando no seu computador.

3. Clone o Repositório
Use o comando `git clone` seguido da URL do repositório que você copiou no Passo 1. O comando completo será semelhante a este:
```markdown
git clone https://github.com/seu-usuario/seu-repositorio.git
```

Substitua a URL pelo URL do repositório que você deseja clonar.

Após executar o comando `git clone`, o Git irá baixar todos os arquivos do repositório remoto para o seu computador e criar uma pasta local com o nome do repositório.

5. Trabalhe no Projeto
Agora que você clonou o repositório, você pode editar, adicionar, e comitar arquivos como faria em qualquer outro projeto Git. Lembre-se de sincronizar suas alterações com o repositório remoto usando `git push` quando você estiver pronto para enviar suas alterações de volta para o GitHub.

Isso é tudo! Você clonou com sucesso um repositório remoto e está pronto para começar a trabalhar no seu projeto localmente.
#### Passo 3: Envie seu código para o repositório remoto
Depois de clonar o repositório ou criar um novo, você pode enviar seu código para o repositório remoto usando os seguintes comandos Git:

```markdown
git add .
git commit -m "Mensagem de commit"
git push origin master
```

Isso adicionará, confirmará e enviará suas alterações para o repositório remoto na branch "master". Certifique-se de substituir "Mensagem de commit" pela mensagem que descreve suas alterações.

E pronto! Agora você tem um repositório remoto no GitHub e seu código está hospedado lá. Você pode compartilhar seu projeto com outras pessoas e colaborar facilmente. Lembre-se de que o GitHub oferece muitos recursos adicionais, como issues, pull requests e colaboração em equipe, para aprimorar o gerenciamento do seu projeto.