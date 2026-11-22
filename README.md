## Iniciar o Front-end:
Abrir um terminal na pasta:

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

## Iniciar o Back-end:

Aceder à pasta do backend:

```powershell
cd Back-end_fca_webbook2-master\fca_webbook2-master
```

Instalar as dependências:

```powershell
npm install
```

O projeto utiliza um ficheiro `node-compat.js` para contornar uma incompatibilidade de uma dependência antiga com o Node.js 26.

O conteúdo desse ficheiro é:

```javascript
const buffer = require('node:buffer');

if (!buffer.SlowBuffer) {
  buffer.SlowBuffer = buffer.Buffer;
}
```

Para iniciar o backend com essa correção:

```powershell
node --require ./node-compat.js app.js
```

**Importante:** o comando anterior foi testado até à fase de inicialização da aplicação e ligação ao MongoDB. O teste terminou com a porta 8080 ocupada por outro processo, pelo que o arranque completo ainda necessita de confirmação.

Para permitir que o professor utilize simplesmente `npm start`, o script `start` do `package.json` do backend deverá ser configurado da seguinte forma:

```json
"scripts": {
  "start": "node --require ./node-compat.js app.js"
}
```
Administrador: admin
Password: 1234
