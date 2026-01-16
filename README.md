
## Estrutura Sugerida do Repositório

```text
portifolio-docker/
├── public-html/          # Pasta com seu HTML, CSS e Imagens
│   ├── index.html
│   ├── style.css
│   └── imagens/
├── nginx.conf            # Configuração do Proxy Reverso
├── docker-compose.yml    # Orquestração dos containers
└── README.md             # Documentação do projeto

```

### **Portfólio Web com Docker & Nginx Proxy**

Este projeto consiste na implantação de uma aplicação web estática (Portfólio) utilizando uma arquitetura de containers orquestrada pelo **Docker Compose**. A solução foca em alta disponibilidade e separação de responsabilidades.

#### **Tecnologias Utilizadas:**

* **Servidor Web:** Apache (`httpd:2.4-alpine`) para servir os arquivos estáticos.
* **Proxy Reverso:** Nginx para gerenciar as requisições na porta 80.
* **Containerização:** Docker & Docker Compose.
* **Frontend:** HTML5, CSS3 e recursos visuais.

#### **Destaques Técnicos:**

* **Persistência de Dados:** Uso de **Volumes (Bind Mounts)** para mapear o código-fonte local diretamente para o diretório `/usr/local/apache2/htdocs/` do Apache, permitindo atualizações em tempo real.
* **Rede Isolada:** Comunicação interna entre Nginx e Apache via rede bridge customizada do Docker.
* **Escalabilidade:** Ambiente facilmente reproduzível em qualquer servidor Ubuntu com Docker instalado.

---

## Como rodar o projeto

Adicione estas instruções para quem baixar seu código:

1. Clone o repositório: `git clone <link-do-seu-repo>`
2. Navegue até a pasta: `cd portifolio-docker`
3. Suba os containers: `docker-compose up -d`
4. Acesse no navegador: `http://localhost` (ou o IP do seu servidor).

---
