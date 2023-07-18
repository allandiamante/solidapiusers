# API REST para Registro de Usuário e Envio de Email de Confirmação

Este é um exemplo de um README simples para uma API REST construída em Node.js utilizando o framework Express. A API permite o registro de usuários e envia um email de confirmação para validar o registro. Os princípios SOLID foram aplicados para promover uma arquitetura sólida e extensível.

## Configuração

Siga as instruções abaixo para configurar e executar a API em seu ambiente local.

### Pré-requisitos

Certifique-se de ter os seguintes requisitos instalados em sua máquina:

- Node.js
- Yarn (gerenciador de pacotes do Node.js)
- Sem Banco de Dados, armazenamento local

### Instalação

1. Clone o repositório para sua máquina local:

   ```bash
   git clone https://github.com/allandiamante/solidapiusers.git
   ```

2. Acesse o diretório do projeto:

   ```bash
   cd solidapiusers
   ```

3. Instale as dependências do projeto usando o NPM:

   ```bash
   npm install
   ```

4. Configure as variáveis de ambiente:

   Crie um arquivo `.env` na raiz do projeto e defina as seguintes variáveis:

   ```env
   PORT=3333
   SMTP_HOST=smtp.exemplo.com
   SMTP_PORT=587
   SMTP_USERNAME=seu-email@exemplo.com
   SMTP_PASSWORD=sua-senha
   ```

   Certifique-se de fornecer os valores corretos para sua configuração.

5. Inicie a API:

   ```bash
   yarn start
   ```

   A API estará disponível em `http://localhost:3333`.

## Utilização

A API fornece os seguintes endpoints:

### Registro de Usuário

**Endpoint:** `POST /users`

Este endpoint permite registrar um novo usuário. O corpo da requisição deve conter os seguintes campos em formato JSON:

```json
{
  "name": "Nome do Usuário",
  "email": "usuario@example.com",
  "password": "senha123"
}
```

Em caso de sucesso, a API retornará um código de status `201 Created` e o seguinte objeto JSON:

```json
{
  "message": "Usuário registrado com sucesso"
}
```
