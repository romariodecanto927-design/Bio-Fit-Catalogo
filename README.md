# 🛋️ Bio-Fit Catálogo - E-commerce de Móveis

## ⚡ Quick Start (Recomendado para Windows)

### Opção 1️⃣: Usar arquivo `.bat` (MAIS FÁCIL)

1. **Abra o Windows Explorer**
2. **Navegue para**: `c:\Users\Usuário\Bio-Fit-Catalogo`
3. **Clique 2x em**: `iniciar.bat`
4. **Aguarde** até ver a mensagem: `🚀 SERVIDOR BIO-FIT RODANDO COM SUCESSO!`
5. **Abra o navegador** em: `http://localhost:3000/index.html`

---

### Opção 2️⃣: Usar PowerShell/Terminal

```powershell
cd "c:\Users\Usuário\Bio-Fit-Catalogo"
npm install
node server.js
```

---

## 🔍 Verificar se está funcionando

### Teste 1: Abra a página de teste
```
http://localhost:3000/teste.html
```

Clique nos botões para testar:
- ✅ Health Check (verifica se servidor responde)
- ✅ Cadastro
- ✅ Login Cliente
- ✅ Login Admin

---

## 👥 Contas de Teste

### Cliente
```
Email: teste@email.com
Senha: senha123
```

### Administrador
```
CPF: 123.456.789-00
Senha: admin123
```

---

## 📁 Estrutura de Arquivos

```
Bio-Fit-Catalogo/
├── index.html                 # Loja virtual
├── admin.html                 # Painel administrativo
├── teste.html                 # Página de teste do servidor
├── server.js                  # Servidor Node.js (backend)
├── package.json               # Dependências Node.js
├── iniciar.bat                # Atalho para iniciar server
├── data/
│   ├── customers.json         # Clientes registrados
│   └── admins.json            # Admins registrados
└── node_modules/              # Bibliotecas Node.js
```

---

## 🚀 Acessar as páginas

| Página | URL |
|--------|-----|
| 🏪 Loja | http://localhost:6500/index.html |
| 🔧 Admin | http://localhost:6500/admin.html |
| 🧪 Teste | http://localhost:6500/teste.html |

---

## ❌ Erros Comuns

### ❌ "Cannot find module 'express'"
**Solução**: Instalar dependências
```powershell
npm install express cors body-parser
```

### ❌ "EADDRINUSE: address already in use :::3000"
**Solução**: Porta 6500 já está em uso
```powershell
# Feche outros programas que usam a porta 3000
# Ou altere a porta no server.js (linha 8)
```

### ❌ "Erro ao conectar com o servidor"
**Solução**: Verifique se o servidor está rodando
```powershell
# Verifique se vê a mensagem:
# 🚀 SERVIDOR BIO-FIT RODANDO COM SUCESSO!
```

### ❌ "CORS error" ou "No 'Access-Control-Allow-Origin' header"
**Solução**: Verifique se a URL está correta
- ✅ Correto: `http://localhost:6500/index.html`
- ❌ Incorreto: `file:///C:/Users/...` (arquivo local)

---

## 🔐 Como usar o sistema

### Para Clientes
1. Abra `http://localhost:6500/index.html`
2. Clique em "Entrar"
3. Escolha "Cliente"
4. **Cadastro**: Preencha nome, email, senha (mín 6 caracteres)
5. **Login**: Use suas credenciais

### Para Administradores
1. Abra `http://localhost:6500/index.html`
2. Clique em "Entrar"
3. Escolha "Admin"
4. Use CPF: `123.456.789-00`, Senha: `admin123`
5. Painel abrirá em `http://localhost:6500/admin.html`

---

## 💾 Banco de Dados

Dados armazenados em **arquivos JSON**:

### customers.json
```json
[
  {
    "id": 1234567890,
    "name": "João Silva",
    "email": "joao@email.com",
    "password": "senha123",
    "createdAt": "2026-06-01T10:30:00Z",
    "orders": []
  }
]
```

### admins.json
```json
[
  {
    "id": 1,
    "cpf": "123.456.789-00",
    "password": "admin123",
    "createdAt": "2026-01-01T00:00:00Z",
    "lastLogin": "2026-06-01T10:30:00Z"
  }
]
```

---

## 🛠️ Dependências do Projeto

```json
{
  "express": "4.18.2",      // Framework web
  "cors": "2.8.5",           // Controle de acesso
  "body-parser": "1.20.2"    // Parser de JSON
}
```

---

## 📝 Notas Importantes

⚠️ **Segurança**:
- Senhas NÃO são criptografadas (apenas para desenvolvimento!)
- Em produção, usar `bcrypt` para hash
- Dados em arquivo JSON (não é banco de dados real)

✅ **Próximas melhorias**:
- Usar banco de dados (SQLite/PostgreSQL)
- Criptografar senhas com bcrypt
- Implementar JWT tokens
- Adicionar verificação de email
- Implementar recuperação de senha

---

## 📞 Suporte

Se tiver problemas:

1. **Verifique se Node.js está instalado**: 
   ```powershell
   node --version
   ```

2. **Verifique se npm está instalado**:
   ```powershell
   npm --version
   ```

3. **Teste o servidor**:
   - Abra: `http://localhost:6500/teste.html`
   - Clique em "Health Check"

4. **Veja os logs do servidor**:
   - Se o servidor estiver rodando, verá mensagens no terminal
   - Procure por erros ou mensagens de aviso

---

**Bio-Fit Catálogo © 2026**