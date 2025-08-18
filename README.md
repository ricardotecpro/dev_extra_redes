# modulo_20_redes

## Curso Intensivo: Infraestrutura Web Moderna para Desenvolvedores

**Domine os Pilares da Web: De Redes e Servidores à Nuvem e Aplicações Escaláveis**

Este curso abrangente foi desenhado por especialistas em engenharia de software e arquitetura de sistemas para fornecer a programadores iniciantes uma base sólida e indispensável sobre a infraestrutura que sustenta a web moderna. Em um mundo onde a linha entre desenvolvimento e operações (DevOps) está cada vez mais tênue, compreender como as aplicações são entregues ao usuário final é um diferencial competitivo crucial.

Ao longo deste curso, você embarcará em uma jornada que desmistifica desde os conceitos fundamentais de redes e da internet até as arquiteturas de nuvem mais avançadas, capacitando-o a construir, implantar e manter aplicações web robustas, seguras e de alta performance.

---

### **Módulo 1: A Fundação - Redes e a Internet**

Neste módulo inicial, construiremos a base do seu conhecimento, explorando os conceitos essenciais que tornam a comunicação global de dados uma realidade.

* **Aula 1: A Mágica da Internet:**
    * O que é a Internet? Uma visão geral de sua história e arquitetura.
    * Modelos de referência: TCP/IP e OSI em uma abordagem simplificada.
    * Pacotes de dados, roteadores e switches: Os carteiros e as agências dos correios da web.

* **Aula 2: Endereçamento na Web - IPs e DNS:**
    * **Endereços IP (Internet Protocol):** A identidade de cada dispositivo na rede.
    * **IP Fixo vs. IP Dinâmico:** Quando e por que usar cada um.
    * **DNS (Domain Name System):** A "lista telefônica" da internet, traduzindo nomes de domínio em endereços IP.
    * **Prática:** Utilizando `ping`, `traceroute` e `nslookup` para diagnosticar conexões e resolver nomes de domínio.

* **Aula 3: Portas, Protocolos e Proxies:**
    * **Portas de Rede:** As portas de entrada e saída para diferentes serviços (HTTP, HTTPS, FTP, SSH).
    * **Protocolos Fundamentais:** HTTP e HTTPS - A linguagem da web.
    * **Servidores Proxy:** O que são, como funcionam e seus diferentes tipos (proxy reverso, proxy forward).

---

### **Módulo 2: O Coração da Aplicação - Servidores Web**

Com a base de redes estabelecida, mergulharemos no software que torna possível servir conteúdo e aplicações aos navegadores dos usuários.

* **Aula 1: Introdução aos Servidores Web:**
    * O papel de um servidor web no ciclo de requisição-resposta.
    * Servidores de conteúdo estático vs. dinâmico.

* **Aula 2: Apache - O Veterano Confiável:**
    * Visão geral da arquitetura do Apache.
    * Instalação e configuração básica (`httpd.conf`).
    * Virtual Hosts: Hospedando múltiplos sites em um único servidor.
    * Módulos essenciais: `mod_rewrite`, `mod_ssl`.

* **Aula 3: Nginx - Performance e Escalabilidade:**
    * A arquitetura orientada a eventos do Nginx.
    * Instalação e configuração (`nginx.conf`).
    * Configurando o Nginx como um servidor web e proxy reverso.
    * Comparativo: Apache vs. Nginx - Quando usar cada um.

* **Aula 4: Laboratório Prático:**
    * Configurando um servidor web local (Apache ou Nginx) para servir um site estático simples.
    * Implementando um proxy reverso com Nginx para uma aplicação Node.js ou Python simples.

---

### **Módulo 3: Desenvolvimento de Aplicações Web - Frontend e Backend**

Neste módulo, conectaremos a infraestrutura com o código, entendendo como as aplicações frontend e backend interagem e se comunicam.

* **Aula 1: A Arquitetura Frontend-Backend:**
    * **Frontend:** A camada de apresentação (HTML, CSS, JavaScript).
    * **Backend:** A lógica de negócios, banco de dados e APIs.
    * A comunicação via APIs RESTful e a importância do JSON.

* **Aula 2: O Papel do Backend na Infraestrutura:**
    * Linguagens e frameworks populares (Node.js, Python/Django/Flask, PHP).
    * Interação com bancos de dados (SQL e NoSQL).
    * Como o servidor web (Apache/Nginx) se comunica com a aplicação backend (ex: via `mod_wsgi`, `gunicorn`, `PHP-FPM`).

* **Aula 3: Frontend e a Rede:**
    * O processo de renderização no navegador.
    * Minificação e concatenação de assets (CSS, JS) para otimização.
    * Requisições assíncronas (AJAX/Fetch API) e seu impacto na experiência do usuário.

---

### **Módulo 4: Entregando Conteúdo em Escala Global - CDNs**

Aprenda a acelerar a entrega do seu conteúdo para usuários em qualquer lugar do mundo, reduzindo a latência e melhorando a performance.

* **Aula 1: O Que é uma CDN (Content Delivery Network)?**
    * O problema da latência e a solução da distribuição geográfica.
    * Como as CDNs armazenam em cache seu conteúdo.

* **Aula 2: Benefícios e Funcionamento:**
    * Melhora na velocidade de carregamento.
    * Redução da carga no servidor de origem.
    * Aumento da segurança com mitigação de ataques DDoS.

* **Aula 3: Na Prática com uma CDN:**
    * Visão geral de provedores populares (Cloudflare, AWS CloudFront).
    * **Prática:** Configurando uma CDN gratuita (Cloudflare) para um site estático, observando a diferença no tempo de resposta.

---

### **Módulo 5: Onde Tudo Acontece - Hospedagem e Implantação**

Explore as diferentes opções para hospedar suas aplicações, desde soluções mais simples e baratas até a infraestrutura elástica e poderosa da nuvem.

* **Aula 1: Opções de Hospedagem:**
    * **Auto-hospedagem e Links Dedicados:** Vantagens, desvantagens e quando considerar.
    * **Hospedagem Compartilhada:** A porta de entrada para iniciantes.
    * **VPS (Virtual Private Server):** O equilíbrio entre custo e controle.
    * **Servidores Dedicados:** Máximo poder e customização.

* **Aula 2: A Revolução da Cloud Computing:**
    * O que é "A Nuvem"? (IaaS, PaaS, SaaS).
    * Principais provedores: AWS, Google Cloud, Microsoft Azure.
    * Vantagens: Escalabilidade, elasticidade, pagamento por uso.

* **Aula 3: Implantação em um VPS:**
    * **Prática:**
        * Provisionando um VPS em um provedor (DigitalOcean, Vultr, etc.).
        * Acessando o servidor via SSH.
        * Instalando e configurando um ambiente LAMP/LEMP (Linux, Apache/Nginx, MySQL, PHP/Python).
        * Implantando uma aplicação web simples.

* **Aula 4: Primeiros Passos na Nuvem (Cloud):**
    * Visão geral de serviços essenciais:
        * **Computação:** AWS EC2, Google Compute Engine.
        * **Armazenamento:** AWS S3, Google Cloud Storage.
        * **Banco de Dados como Serviço:** AWS RDS, Google Cloud SQL.
    * Introdução à infraestrutura como código (IaC) e conteinerização (Docker).

---

### **Projeto Final: Do Código à Implantação Global**

Para consolidar todo o conhecimento adquirido, os alunos desenvolverão um projeto prático que abrange todas as etapas do curso:

1.  **Desenvolvimento:** Criar uma aplicação web simples (ex: um blog ou um portfólio) com um frontend e um backend.
2.  **Hospedagem:** Provisionar um servidor VPS.
3.  **Configuração:** Instalar e configurar o Nginx como servidor web e proxy reverso para a aplicação.
4.  **Implantação:** Publicar a aplicação no VPS.
5.  **Domínio e DNS:** Apontar um nome de domínio para o IP do servidor.
6.  **Otimização:** Integrar a aplicação com uma CDN para acelerar a entrega do conteúdo estático.
7.  **Segurança:** Configurar um certificado SSL/TLS (Let's Encrypt) para habilitar o HTTPS.

Ao final deste curso, você não será apenas um programador, mas um desenvolvedor com uma visão holística do ecossistema web, preparado para tomar decisões de arquitetura mais inteligentes e construir aplicações que não apenas funcionam, mas que são performáticas, escaláveis e seguras.
