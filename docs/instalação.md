# ⚙️ Instalação do Wazuh

## 📌 Ambiente

* Sistema: Rocky Linux
* Virtualização: VirtualBox
* Acesso remoto: PuTTY

---

## 📥 Download do Wazuh

Comando utilizado:

```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
```

### Parâmetros utilizados

```bash
sudo bash wazuh-install.sh -a
```

### 🔎 Explicação

* `-a` → Instala tudo automaticamente:

  * Wazuh Manager
  * Indexer
  * Dashboard

---

## ⚠️ Ignorar verificações de compatibilidade

Como Rocky Linux pode não ser oficialmente suportado:

```bash
sudo bash wazuh-install.sh -a -i
```

* `-i` → Ignora verificações do sistema operacional (force install)

---

## 🌐 Acesso ao Dashboard

Após instalação:

```
https://IP_DO_SERVIDOR
```

Exemplo fictício:

```
https://192.168.100.10
```

