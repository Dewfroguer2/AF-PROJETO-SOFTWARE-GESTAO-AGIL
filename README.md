# Front-end de avaliações

## Configurar o computador para desenvolvimento

Instale Node.js 22 ou superior e Python 3. Depois, no PowerShell, abra este repositório e defina as variáveis da sua sessão (substitua os exemplos):

```powershell
$env:AUTH0_DOMAIN = "seu-tenant.auth0.com"
$env:AUTH0_CLIENT_ID = "client-id-da-aplicacao-spa"
$env:AUTH0_AUDIENCE = "identificador-da-api-configurado-no-auth0"
$env:API_BASE_URL = "http://localhost:8080"
npm run build
python -m http.server 5500 --directory dist
```

Abra `http://localhost:5500`. Adicione esse endereço às **Allowed Callback URLs**, **Allowed Logout URLs** e **Allowed Web Origins** da aplicação SPA Auth0. A audience é obrigatória para obter o token da API. As variáveis definidas com `$env:` valem apenas naquela sessão do PowerShell. 
