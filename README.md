# 🛡️ Wazuh SIEM - Instalação em Rocky Linux (Lab)



\

---

## 📌 Sobre o Projeto

Este repositório documenta a instalação e configuração do **Wazuh SIEM** em ambiente de laboratório utilizando **Rocky Linux**, com foco em aprendizado prático de **segurança da informação** e **monitoramento de eventos**.

---

## 🧱 Arquitetura do Ambiente

```
[ Máquina Host ]
        │
        ▼
[ VirtualBox ]
        │
        ▼
[ Rocky Linux VM ]
        │
        ├── Wazuh Manager
        ├── Wazuh Indexer
        └── Wazuh Dashboard
```

---

## 🖥️ Especificações da Máquina Virtual

| Recurso | Configuração |
| ------- | ------------ |
| CPU     | 2 vCPUs      |
| Memória | 6 GB RAM     |
| Disco   | 50 GB        |
| Rede    | Bridge       |
| Acesso  | SSH (PuTTY)  |

---

## 🌐 Rede

* IP (exemplo): `192.168.100.10`

---

## ⚙️ Instalação do Wazuh

### 📥 Baixar instalador

```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
```

### ▶️ Executar instalação

```bash
sudo bash wazuh-install.sh -a -i
```

### 📌 Parâmetros utilizados

| Parâmetro | Descrição                                         |
| --------- | ------------------------------------------------- |
| `-a`      | Instalação All-in-One (todos os componentes)      |
| `-i`      | Ignora verificações de compatibilidade do sistema |

---

## 🔐 Acesso ao Dashboard

```
https://192.168.100.10:443
```

**Credenciais:**

* Usuário: `admin`
* Senha: `SenhaFicticia@123`

---

## 🔥 Configuração do Firewall

### Liberar HTTPS

```bash
sudo firewall-cmd --add-service=https --permanent
sudo firewall-cmd --reload
```

### Liberar portas dos agentes

```bash
sudo firewall-cmd --add-port=1514/tcp --permanent
sudo firewall-cmd --add-port=1514/udp --permanent
sudo firewall-cmd --add-port=1515/tcp --permanent
sudo firewall-cmd --reload
```

---

## 🧩 Agentes

Acesse:

```
https://192.168.100.10/app/wazuh#/agents-preview
```

---

## 🧪 Teste de Eventos

No Windows (CMD):

```cmd
net user hacker123 123456 /add
```

✔️ Deve gerar alerta no Wazuh

---

## ⚠️ Troubleshooting

### Dashboard não abre

* Verificar firewall (porta 443)

### Agente não conecta

* Verificar portas 1514 e 1515
* Verificar conectividade de rede

### Lentidão

* Verificar recursos da VM (RAM/CPU)

---

## 📚 Conceitos Importantes

* **SIEM:** Sistema de monitoramento e correlação de eventos de segurança
* **Agent:** Software instalado no endpoint para envio de logs
* **Manager:** Responsável por processar eventos
* **Indexer:** Armazena e indexa logs
* **Dashboard:** Interface visual

---

## 🚀 Roadmap

* [ ] Integração com Grafana
* [ ] Criação de regras customizadas
* [ ] Monitoramento avançado
* [ ] Hardening do ambiente
* [ ] Integração com outras ferramentas (ex: threat intelligence)

---

## 📎 Observações

* Ambiente voltado para **estudos e laboratório**
* Para produção, recomenda-se arquitetura distribuída

---

## 👨‍💻 Autor

Projeto desenvolvido por **Rafael Francisco**
📚 Estudante de Análise e Desenvolvimento de Sistemas
🔐 Foco em Segurança da Informação

---

## ⭐ Contribuição

Sinta-se livre para abrir issues ou contribuir com melhorias 🚀

---

