Neste guia, vamos passar pelo processo de configuração de um projeto Node.js, começando com a criação do arquivo `package.json` usando o comando `npm init`.

## Passo 1: Criação do Projeto
Primeiro, crie uma pasta para o seu projeto e navegue até ela usando o terminal:

```bash
mkdir meu-projeto-node
cd meu-projeto-node
```

## Passo 2: Inicialização do `package.json`
Use o comando `npm init` para criar o arquivo `package.json`. Este arquivo conterá informações sobre o seu projeto, como nome, versão, descrição e muito mais. Você pode responder às perguntas interativas ou simplesmente pressionar Enter para aceitar as configurações padrão:

```bash
npm init
```

## Passo 3: Instalação de Dependências
Agora que você tem o `package.json` configurado, você pode começar a instalar dependências para o seu projeto. Por exemplo, vamos instalar o pacote `express`, um popular framework web para Node.js:

```bash
npm install express
```

Isso instalará o pacote `express` e adicionará uma entrada no seu `package.json` sob a seção `"dependencies"`.

## Passo 4: Criação de um Arquivo de Código
Crie um arquivo JavaScript para o seu código. Por exemplo, `app.js`:

```javascript
// app.js
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Olá, Mundo!');
});

app.listen(3000, () => {
  console.log('O servidor está rodando na porta 3000.');
});
```

## Passo 5: Execução do Projeto
Agora que você tem um arquivo de código, você pode executar o seu projeto. Use o seguinte comando para iniciar o servidor:

```bash
node app.js
```

Acesse `http://localhost:3000` em seu navegador e você verá a mensagem "Olá, Mundo!".

## Passo 6: Utilização do `package-lock.json`
Ao instalar pacotes, o npm automaticamente cria um arquivo chamado `package-lock.json`. Este arquivo registra a árvore exata de dependências e suas versões. Isso ajuda a garantir a consistência das versões em diferentes ambientes.

## Conclusão
Agora você tem um projeto Node.js básico configurado! Você pode continuar adicionando mais dependências, escrevendo seu código e personalizando seu projeto de acordo com suas necessidades.

Lembre-se de sempre verificar o seu `package.json` para garantir que todas as dependências estejam listadas corretamente.

Espero que este guia tenha sido útil para você começar com o Node.js!
```
Você pode copiar e colar este tutorial em um arquivo Markdown (.md) e usar um visualizador Markdown ou ferramenta de documentação para ver o resultado formatado. Lembre-se de substituir `meu-projeto-node` pelo nome do seu projeto e ajustar os detalhes de acordo com suas necessidades específicas.
```