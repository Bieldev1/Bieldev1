<h1 align="center">Gabriel Rocha Santos</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=1000&color=2E8B57&center=true&vCenter=true&width=600&lines=Desenvolvedor+Full+Stack+.NET;C%23+%C2%B7+ASP.NET+Core+%C2%B7+Vue.js+%C2%B7+Azure;Clean+Architecture+%C2%B7+CQRS+%C2%B7+DDD+em+produ%C3%A7%C3%A3o" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://portifolio-umber-eight.vercel.app"><img src="https://img.shields.io/badge/Portfólio-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://linkedin.com/in/gabriel-rocha-santos-105484230"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://wa.me/5511963854807"><img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" /></a>
</p>

---

### Sobre

Atuo como **Desenvolvedor Full Stack** na **Viktech**, onde sou o único responsável de ponta a ponta por **4 projetos estratégicos** em produção desde novembro de 2025 — arquitetura, desenvolvimento, deploy e manutenção.

No dia a dia, trabalho com:

- **Clean Architecture, CQRS e DDD** em sistemas com regras de negócio complexas
- **ASP.NET Core Identity** com **MFA e RBAC** para controle de acesso granular
- **Integrações de alta criticidade**: WhatsApp Business, C6 Bank, OpenAI, Google Maps, Correios — incluindo **filas e throttling** para proteger disponibilidade em cenários de alto volume
- **Entity Framework Core** e **Vue.js** no front, fechando o ciclo full stack

Atualmente cursando **Tecnólogo em Análise e Desenvolvimento de Sistemas** (conclusão prevista em 2027), aprofundando fundamentos enquanto aplico tudo em produção real.

---

### Stack

**Backend**
<p>
<img src="https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white" />
<img src="https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/ASP.NET_Core-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/Entity_Framework_Core-512BD4?style=flat-square&logo=dotnet&logoColor=white" />
<img src="https://img.shields.io/badge/MediatR-CQRS-blue?style=flat-square" />
</p>

**Frontend**
<p>
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vue.js&logoColor=white" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
</p>

**Dados & Mensageria**
<p>
<img src="https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white" />
</p>

**Cloud & DevOps**
<p>
<img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=white" />
</p>

**Arquitetura & Práticas**
<p>
<img src="https://img.shields.io/badge/Clean_Architecture-black?style=flat-square" />
<img src="https://img.shields.io/badge/DDD-black?style=flat-square" />
<img src="https://img.shields.io/badge/CQRS-black?style=flat-square" />
<img src="https://img.shields.io/badge/Result_Pattern-black?style=flat-square" />
<img src="https://img.shields.io/badge/xUnit-Testing-purple?style=flat-square" />
</p>

---

### GitHub

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=Bieldev1&theme=transparent&hide_border=true&ring=2E8B57&fire=2E8B57&currStreakLabel=2E8B57" />
</p>

---

### Projetos em destaque

**[SmartCommerce](https://github.com/Bieldev1/smart-commerce)** — plataforma de e-commerce com chat de suporte em tempo real (SignalR) e assistente de produto via IA (Groq/Gemini), construída em Clean Architecture com CQRS e DDD.

- Domain layer isolado, sem dependências externas — Entities, Value Objects, Aggregates, Domain Events
- Abstração de provider de IA (`IAIProvider`): troca entre Groq e Gemini sem tocar em regra de negócio
- SignalR com sessões isoladas por cliente via Hub Groups
- ASP.NET Core Identity com JWT + Refresh Token + RBAC (Admin/Customer/Support)
- Testes unitários e de integração (xUnit + Moq), setup completo via Docker Compose

🔗 [Demo ao vivo](https://smart-commerce-delta.vercel.app) · [Código](https://github.com/Bieldev1/smart-commerce)

<br />

**[NotificationHub](https://github.com/Bieldev1/notification-hub)** — hub de notificações multi-canal com fila assíncrona (RabbitMQ), retry configurável e Dead Letter Queue, 100% containerizado.

- Domain isolado sem dependências externas — Result Pattern e `Entity<TId>` com igualdade por Id, CQRS com MediatR
- Desacopla aceitar o pedido de processá-lo: a API responde na hora, uma fila dedicada processa o envio, com retry automático e Dead Letter Queue em caso de falha persistente
- Integração real de e-mail via API REST (Brevo), com provider mockável selecionável por configuração para dev local
- Dockerfile multi-stage (SDK → runtime) + `docker-compose` orquestrando API, PostgreSQL e RabbitMQ, com retry/backoff de conexão para lidar com race conditions de healthcheck
- Testes unitários (xUnit + Moq) cobrindo entidade, Result Pattern e o handler de negócio

🔗 [Código](https://github.com/Bieldev1/notification-hub)

---

### Contato

📱 [WhatsApp](https://wa.me/5511963854807) · 💼 [LinkedIn](https://linkedin.com/in/gabriel-rocha-santos-105484230) · 🌐 [Portfólio](https://portifolio-umber-eight.vercel.app)
