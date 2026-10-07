### Como abrir o OutBreak

O OutBreak é um projeto web completo, então **não basta clicar duas vezes no `index.html`**. O jogo possui vários arquivos JavaScript, arquivos CSS, imagens, componentes e outras dependências que precisam ser carregadas pelo navegador da maneira correta.

Primeiro, **extraia o ZIP inteiro** para uma pasta no computador. Não mova ou separe o `index.html`, os arquivos `.js` ou o `style.css` para outras pastas, porque o projeto utiliza caminhos entre esses arquivos.

Depois, abra a pasta principal do OutBreak no **Visual Studio Code**.

Com a pasta aberta, abra o terminal do VS Code em:

**Terminal → Novo Terminal**

No terminal, execute:

```bash
npm install
```

Esse comando instala todas as dependências necessárias para o projeto funcionar.

Depois que terminar, execute:

```bash
npm run dev
```

O projeto será iniciado por um servidor local. O terminal vai mostrar um endereço parecido com:

```text
http://localhost:5173/
```

Abra esse endereço no navegador.

### Por que fazer isso?

Quando você abre o `index.html` diretamente, usando algo como `file:///C:/.../index.html`, o navegador não trata o projeto como uma aplicação web completa. Alguns módulos JavaScript, imports, recursos e funcionalidades podem não funcionar corretamente. O resultado pode ser uma página sem estilo, com botões quebrados, animações que não aparecem ou partes do jogo que simplesmente não carregam.

Usando `npm run dev`, o servidor organiza o projeto corretamente e permite que o **HTML, CSS e JavaScript trabalhem juntos**, incluindo os arquivos que estão dentro das subpastas.

### Importante

Não apague nem renomeie arquivos do projeto sem saber para que eles servem. Mantenha a estrutura original das pastas.

Sempre que quiser iniciar o OutBreak novamente, basta abrir a pasta no VS Code e executar:

```bash
npm run dev
```

Depois, acesse o endereço `localhost` mostrado no terminal.

**Resumindo:** não abra o `index.html` diretamente. Abra a pasta do projeto no VS Code, instale as dependências com `npm install` e execute o jogo com `npm run dev`. Assim o OutBreak será carregado como um projeto completo, com HTML, CSS, JavaScript, animações e todas as funcionalidades funcionando em conjunto.
