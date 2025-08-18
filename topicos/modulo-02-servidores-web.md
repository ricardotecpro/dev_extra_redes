### **Arquivo 2: `modulo-02-servidores-web.md`**

```markdown
# 🚀 Módulo 2: O Coração da Aplicação - Servidores Web

Agora que entendemos como a informação viaja pela rede, vamos focar no software que a recebe e responde: o servidor web. Ele é a porta de entrada para sua aplicação.

## 🔄 Aula 1: Introdução aos Servidores Web

### O Ciclo Requisição-Resposta
Toda interação na web segue este fluxo fundamental:
1.  O **cliente** (navegador) faz uma **requisição** HTTP para um servidor.
2.  O **servidor web** processa a requisição.
3.  O servidor envia uma **resposta** HTTP de volta ao cliente.
4.  O cliente renderiza a resposta (ex: exibe uma página HTML).

```mermaid
sequenceDiagram
    participant Client as "Cliente (Navegador)"
    participant Server as "Servidor Web (Nginx/Apache)"
    participant App as "Aplicação Backend"

    Client->>Server: GET /pagina.html HTTP/1.1
    Note over Server: Requisição recebida
    Server-->>Client: HTTP/1.1 200 OK\n<html>...</html>
    Note over Client: Resposta recebida e renderizada

    Client->>Server: GET /api/dados HTTP/1.1
    Server->>App: Processar requisição para /api/dados
    App-->>Server: Dados em JSON
    Server-->>Client: HTTP/1.1 200 OK\n{"id": 1, "nome": "Produto"}
````

  - **Conteúdo Estático:** Arquivos que não mudam (HTML, CSS, JS, imagens). Servidos diretamente pelo servidor web.
  - **Conteúdo Dinâmico:** Conteúdo gerado na hora por uma aplicação (ex: um feed de notícias). O servidor web repassa a requisição para a aplicação.

## 🔥 Aula 2: Apache - O Veterano Confiável

O **Apache HTTP Server** é um dos servidores web mais antigos e populares. É conhecido por sua flexibilidade e enorme quantidade de módulos.

  - **Arquitetura:** Baseada em processos ou threads.
  - **Configuração:** O arquivo principal é o `httpd.conf`. As configurações de sites específicos geralmente ficam em `sites-available`.
  - **Virtual Hosts:** Permite hospedar múltiplos domínios (`site1.com`, `site2.com`) no mesmo servidor e IP.

**Exemplo de Virtual Host no Apache:**

```apache
<VirtualHost *:80>
    ServerName [www.meusite.com](https://www.meusite.com)
    ServerAdmin webmaster@meusite.com
    DocumentRoot /var/www/[meusite.com/public_html](https://meusite.com/public_html)

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

  - **Módulos Essenciais:**
      - `mod_rewrite`: Para reescrever URLs.
      - `mod_ssl`: Para habilitar HTTPS.

## ⚡ Aula 3: Nginx - Performance e Escalabilidade

**Nginx** (pronuncia-se "Engine-X") é um servidor web moderno, conhecido por sua alta performance, baixo consumo de recursos e capacidade de lidar com milhares de conexões simultâneas.

  - **Arquitetura:** Orientada a eventos, assíncrona.
  - **Configuração:** O arquivo principal é o `nginx.conf`.
  - **Usos Comuns:** Além de servidor web, é amplamente utilizado como **proxy reverso**, **balanceador de carga** e **cache HTTP**.

**Exemplo de Bloco de Servidor (Server Block) no Nginx:**

```nginx
server {
    listen 80;
    server_name [www.meusite.com](https://www.meusite.com);

    root /var/www/[meusite.com/public_html](https://meusite.com/public_html);
    index index.html index.htm;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

### Apache vs. Nginx

  - **Apache:** Ótimo para flexibilidade, hospedagem compartilhada e configurações complexas com `.htaccess`.
  - **Nginx:** Brilha ao servir conteúdo estático, como proxy reverso e em cenários de alta concorrência. É a escolha mais comum para arquiteturas modernas.

## 🔧 Aula 4: Laboratório Prático

Nesta aula prática, vamos colocar a mão na massa\!

1.  **Instalar Nginx ou Apache:** Use o gerenciador de pacotes do seu sistema (ex: `sudo apt install nginx`).
2.  **Configurar um Site Estático:**
      - Crie um diretório para seu site (ex: `/var/www/meu-site`).
      - Crie um arquivo `index.html` dentro dele.
      - Configure um virtual host (Apache) ou server block (Nginx) apontando para esse diretório.
3.  **Configurar um Proxy Reverso com Nginx:**
      - Suponha que você tem uma aplicação Node.js rodando na porta 3000.
      - Configure o Nginx para receber requisições na porta 80 e repassá-las para `localhost:3000`.

**Exemplo de Proxy Reverso no Nginx:**

```nginx
server {
    listen 80;
    server_name minhaapi.com;

    location / {
        proxy_pass http://localhost:3000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}
```

````
