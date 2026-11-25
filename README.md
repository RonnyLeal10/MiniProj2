## Pré-requisitos

- Node.js e npm instalados.
- MongoDB instalado e em execução.
- Base de dados original do Animalec importada para a base de dados local `animalec`.

## Iniciar o Back-end

Abrir um terminal na pasta principal do projeto e aceder à pasta do backend:

```powershell
cd Back-end_fca_webbook2-master\fca_webbook2-master
```

Instalar as dependências:

```powershell
npm install
```

Iniciar o servidor:

```powershell
npm start
```

O backend ficará disponível em:

http://localhost:8080

A ligação à base de dados MongoDB é efetuada através de:

```text
mongodb://localhost:27017/animalec
```

O projeto inclui o ficheiro `node-compat.js`, que permite contornar uma incompatibilidade de uma dependência antiga com o Node.js 26. Esta correção é aplicada automaticamente através do comando `npm start`, não sendo necessária qualquer configuração adicional do script de arranque.

## Iniciar o Front-end

Abrir um novo terminal na pasta principal do projeto e aceder à pasta do frontend:

```powershell
cd Front-end_Animalec-master
```

Instalar as dependências:

```powershell
npm install
```

Iniciar o servidor de desenvolvimento:

```powershell
$env:NODE_OPTIONS="--openssl-legacy-provider"; npm run serve
```

Aceder ao endereço apresentado no terminal através do navegador.

## Credenciais de acesso local

- **Administrador:** admin
- **Password:** 1234

Estas credenciais destinam-se exclusivamente ao ambiente local de demonstração.

## Validação do projeto

Após a atualização das dependências, foram testadas com sucesso as seguintes funcionalidades:

- Autenticação do administrador;
- Consulta, adição e edição de animais;
- Gestão de utilizadores;
- Gestão de especialistas (Experts);
- Gestão de patrocinadores (Sponsors);
- Consulta de perguntas e quizzes;
