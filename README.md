# gercom_testes-ipc-grpc-socket

Repositório que reúne as bancadas experimentais preliminares de **comunicação entre processos (IPC)**, **sockets TCP** e chamadas de procedimento remoto distribuídas (**gRPC / Protocol Buffers**), desenvolvidas no âmbito do **Laboratório GERCOM / UFPA**.

Estes protótipos serviram como fundação técnica de rede para a concepção e implementação do framework **FedT (Federated Trees)**.

---

## 📂 Módulos e Bancadas

1. **`Testes Socket/`:**
   - Implementação de baixo nível com a Python Socket API (`socket.AF_INET`, `socket.SOCK_STREAM`).
   - Servidor concorrente e cliente TCP com troca de mensagens textuais e controle de fluxo.
2. **`gRPC/`:**
   - **`Teste 01/`:** Primeiro contrato `.proto` (`teste01.proto`), compilação de stubs Python (`teste01_pb2.py`, `teste01_pb2_grpc.py`) e chamada unária básica cliente-servidor.
   - **`Teste 02/`:** Evolução de mensagens tipadas e tratamento de requisições estruturadas.
   - **`Teste 03 - Multiplos Clientes/`:** Orquestração de múltiplos clientes simultâneos conectando ao mesmo servidor gRPC (`multclient.proto`), validando a concorrência assíncrona necessária para aprendizado federado.

---

## 🛠️ Tecnologias

- **Python 3.9+**
- **gRPC (`grpcio`) & Protocol Buffers (`protobuf`)**
- **Python Socket API**

---

## 📄 Licença
Distribuído sob a licença MIT. Veja `LICENSE` para mais detalhes.
