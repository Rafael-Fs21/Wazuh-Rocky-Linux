# 🧪 Testes e geração de alertas

## 📌 Objetivo

Gerar eventos para validar o funcionamento do SIEM.

---

## 💣 Teste 1 - Tentativa de usuário inválido

```cmd
net user hacker123 123456 /add
```

---

## 💣 Teste 2 - Tentativa de acesso inválido

```cmd
runas /user:fakeuser cmd
```

---

## 💣 Teste 3 - Falha de login

```cmd
net use \\127.0.0.1 /user:usuario_errado
```

---

## 📊 Resultado esperado

* Eventos aparecem no dashboard
* Alertas são gerados automaticamente
* Logs classificados por nível de risco

---

## 🧠 Observação

Esses testes simulam comportamentos comuns de ataque:

* Criação de usuário suspeito
* Tentativas de acesso indevido

