# 🔧 Configuração do Wazuh

## 🔥 Liberação de firewall

Caso não consiga acessar via navegador:

```bash
sudo systemctl stop firewalld
```

Ou liberar portas específicas (recomendado em produção).

---

## 📡 Conexão do agente

Instalação do agente na máquina cliente:

```bash
WAZUH_MANAGER="192.168.100.10" sudo bash wazuh-agent.sh
```

---

## 🔗 Verificação

No dashboard:

* Vá em **Agents**
* Verifique se está:

  * Status: Active

---

## 🧠 Funcionamento

O agente envia logs para o servidor Wazuh, que:

* Analisa eventos
* Aplica regras
* Gera alertas


