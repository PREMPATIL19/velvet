# Velvet

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

A documentação completa será publicada em:

📎 [`https://velvet.network/docs`](https://velvet.network/docs) *(em construção)*

Documentos técnicos e diagrama de arquitetura estão disponíveis na pasta `docs/`.

## Contribuindo

Quer ajudar? Veja o [CONTRIBUTING.md](CONTRIBUTING.md) para guidelines e padrões de contribuição. Pull requests são muito bem-vindos!

## Licença

Licenciado sob os termos da [Apache LICENSE](LICENSE).

> *“Velvet conecta dados, pessoas e paixões em torno de um mesmo universo.”*