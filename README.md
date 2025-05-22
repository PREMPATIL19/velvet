<div align="center">

  <img src="/assets/logo.png" width="150" height="150" />

  # Velvet

  [![License: Apache License 2.0](https://img.shields.io/badge/license-Apache%20License%202.0-blue?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
  [![Favoritados](https://img.shields.io/github/stars/uesleibros/velvet?style=flat-square)](https://github.com/uesleibros/velvet/stargazers)
  [![Tam. Código](https://img.shields.io/github/languages/code-size/uesleibros/velvet?style=flat-square)](https://github.com/uesleibros/velvet)
  [![Contribuidores](https://img.shields.io/github/contributors/uesleibros/velvet?style=flat-square)](https://github.com/uesleibros/velvet/graphs/contributors)
  [![Issues](https://img.shields.io/github/issues/uesleibros/velvet?style=flat-square)](https://github.com/uesleibros/velvet/issues) \
  [![Pull Requests](https://img.shields.io/github/issues-pr/uesleibros/velvet?style=flat-square)](https://github.com/uesleibros/velvet/pulls)
  [![Commit Activity](https://img.shields.io/github/commit-activity/t/uesleibros/velvet?style=flat-square)](https://github.com/uesleibros/velvet/commits/main)
  [![Last Commit](https://img.shields.io/github/last-commit/uesleibros/velvet?style=flat-square)](https://github.com/uesleibros/velvet/commits/main) \
  [![Made with Love](https://img.shields.io/badge/feito%20com-amor-pink?style=flat-square)](https://github.com/uesleibros/velvet/graphs/contributors)

</div>

**Velvet** é uma plataforma full-stack descentralizada para exploração, curadoria e automação de conteúdo relacionado a anime. Integrando tecnologias modernas e arquitetura modular, Velvet conecta múltiplas fontes externas e redes comunitárias, entregando uma experiência consistente e escalável através de Web, API e bots.

## Visão Geral

Velvet opera como uma **rede descentralizada**, onde o backend atua como orquestrador e agregador de dados, distribuindo e sincronizando informações com plataformas como **Anilist**, **MyAnimeList**, **LiveChart**, **Kitsu**, **Crunchyroll**, entre outras.

## Arquitetura

```text
                 +----------------+
                 |    Frontend    | ← Web App em React + Tailwind
                 +--------+-------+
                          |
                          ▼
                 +--------+-------+
                 |   API Python   | ← Backend modular (REST/GraphQL)
                 +--------+-------+
                          |
          +---------------+---------------+
          |                               |
          ▼                               ▼
+----------------+              +-----------------------+
|   Bot (Rust)   | ← Discord    |   Data Providers      |
| (Serenity lib) |────────────▶ | (Anilist, MAL, etc.)  |
+----------------+    eventos   +-----------------------+
          |
          ▼
+----------------+
|  API Python    | ← Interações com bot (commands, webhooks)
+----------------+

          ▼
+------------------------+
| Database & Cache       |
| (PostgreSQL, Redis...) |
+------------------------+
```

## Tecnologias

| Camada       | Stack                                  |
| ------------ | -------------------------------------- |
| **Frontend** | TypeScript, React, TailwindCSS         |
| **Backend**  | Python, PostgreSQL, Supabase, ...      |
| **Bot**      | Rust (`serenity`, `twilight`)          |
| **Cache**    | HTTP caching                           |
| **DevOps**   | Docker, GitHub Actions, NGINX, systemd |
| **Infra**    | VPS/Linux, Cloudflare, Render/AWS      |

## Funcionalidades

* 📚 **Integração com múltiplas APIs** de anime (Anilist, MAL, etc)
* 💬 **Bot Discord modular** com comandos, eventos e webhooks
* 🔍 **Busca inteligente** e filtros avançados de animes
* ⚙️ **Painel administrativo** para gerenciar dados e usuários
* 🌐 **Frontend responsivo** com performance otimizada
* 📈 **Recomendações baseadas em histórico e perfil**
* 🔐 **Camada de autenticação segura** via OAuth2 / JWT

## Instalação Local

1. Clone o repositório:

```bash
git clone https://github.com/uesleibros/velvet.git
cd velvet
```

3. Inicie os serviços:

```bash
# Backend
cd apps/backend
cargo run

# Bot
cd apps/assistant
cargo run

# Frontend
cd frontend
npm install && npm run dev
```

## Testes

```bash
# Testes unitários e de integração no backend
cargo test --all
```

## Documentação

Documentos técnicos e diagrama de arquitetura estão disponíveis na pasta `docs/`.

## Contribuindo

Quer ajudar? Veja o [CONTRIBUTING.md](CONTRIBUTING.md) para guidelines e padrões de contribuição. Pull requests são muito bem-vindos!

## Licença

Licenciado sob os termos da [Apache LICENSE](LICENSE).

> *“Velvet conecta dados, pessoas e paixões em torno de um mesmo universo.”*
