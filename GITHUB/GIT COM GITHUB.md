## Guia de Fluxo Git

1. **Criação de um Repositório Remoto no GitHub**
   - No GitHub, crie um novo repositório remoto.

2. **Clone do Repositório Remoto (Branch Master/main)**
   - Clone o repositório remoto para o seu ambiente local usando:
     ```shell
     git clone <url-do-repositorio>
     ```

3. **Trabalho/Desenvolvimento do Projeto**
   - Realize o desenvolvimento do seu projeto.

4. **Adição de Alterações à Área de Staging (Git add)**
   - Adicione as alterações desejadas à área de staging usando:
     ```shell
     git add <nome-do-arquivo>
     git add .
     ```

5. **Consolidação das Alterações (Git commit)**
   - Consolide as alterações na área de staging com um comentário descritivo:
     ```shell
     git commit -m "comentário"
     ```

6. **Sincronização com o Repositório Remoto (Git push origin)**
   - Sincronize as alterações com o repositório remoto usando:
     ```shell
     git push origin master
     git push
     git push origin master --force
     ```

## Guia de Comandos

1. **Verificação da Instalação do Git e Versão**
   - Verifique se o Git está instalado e veja sua versão usando:
     ```shell
     git --version
     ```

2. **Configuração de Variáveis**
   - Configure variáveis de usuário global ou localmente usando:
     ```shell
     git config --global user.email you@example.com
     git config --global user.name "Your Name"
     ```
     ou
     ```shell
     git config --local user.email you@example.com
     git config --local user.name "Your Name"
     ```

   - **--global** → Configuração global para a máquina toda
   - **--local** → Configuração local para o projeto

   - Visualize configurações válidas para o projeto usando:
     ```shell
     git config user.name
     git config user.email
     ```

   - Erro de Certificado SSL:
     ```shell
     git config --global http.sslbackend schannel
     ```

3. **Inicialização de um Repositório**
   - Inicialize um repositório local usando:
     ```shell
     git init
     git status
     ```

4. **Adição de Arquivos ao Staging**
   - Adicione arquivos à área de staging usando:
     ```shell
     git add <nome-do-arquivo>
     git add .
     ```

6. **Consolidação de Alterações**
   - Consolide as alterações com um comentário usando:
     ```shell
     git commit -m "comentário"
     ```

7. **Vinculação a um Repositório Remoto**
   - Associe um repositório remoto usando:
     ```shell
     git remote add origin <url-do-repositorio>
     git remote -v
     ```

8. **Envio de Alterações para o Repositório Remoto (Sincronização)**
   - Sincronize com o repositório remoto usando:
     ```shell
     git push -u origin master
     git push
     git push origin master --force
     ```

9. **Clone de um Repositório Remoto**
   - Clone um repositório remoto usando:
     ```shell
     git clone <url-do-repositorio>
     ```
