# 🛠️ Troubleshooting

## ❌ Não acessa o dashboard

### Possível causa:

Firewall bloqueando

### Solução:

```bash
sudo systemctl stop firewalld
```

---

## ❌ Agente não aparece

### Possíveis causas:

* IP incorreto
* Porta bloqueada
* Serviço parado

### Solução:

```bash
systemctl status wazuh-agent
```

---

## ❌ Dashboard não carrega

### Verificar:

* Serviço do Wazuh
* Conectividade de rede

---

## 🧠 Dica

Sempre validar:

* IP do servidor
* Comunicação entre máquinas
* Status dos serviços

