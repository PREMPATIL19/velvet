# Contribuindo para o Velvet

Agradecemos seu interesse em contribuir com o **Velvet**! Este projeto é uma plataforma descentralizada e modular, então manter a consistência e a qualidade do código é fundamental.

## Visão Geral

Velvet é dividido em múltiplos apps e bibliotecas:

- `apps/frontend`: Interface web (React + Tailwind)
- `apps/backend`: API principal (Python + FastAPI)
- `apps/assistant`: Bot do Discord (Rust)
- `packages/`: Módulos utilitários compartilhados
- `tests/`: Testes automatizados

## Como começar

1. **Fork o repositório**
2. **Clone o fork**
   ```bash
   git clone https://github.com/uesleibros/velvet.git
   cd velvet
   ```
3. **Crie uma branch para sua feature/fix**
   ```bash
   git checkout -b feat/nome-da-sua-feature
   ```

## Rodando localmente

Consulte os `README.md` dentro de cada `apps/` para setup individual.

### Requisitos gerais:
- Node.js 18+
- Python 3.11+ com `poetry`
- Rust stable (`rustup`)
- PostgreSQL + Redis em background

## Commits e Convention

Utilizamos [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```
feat: nova funcionalidade
fix: correção de bug
chore: mudanças internas (infra, deps)
refactor: melhoria sem mudança funcional
docs: alterações em documentação
test: adição ou ajuste de testes
```

Exemplo:
```
feat(backend): adicionar suporte a cache no endpoint de busca
```

## Estilo de Código

### Python
- Siga o [PEP8](https://peps.python.org/pep-0008/)
- Use `ruff` e `black` antes de commitar

### Rust
- Formate com `cargo fmt`
- Lint com `cargo clippy`

### JavaScript/TypeScript
- ESLint + Prettier (já configurados no projeto)

## Testes

Crie testes para novas funcionalidades quando aplicável.

```bash
# Python
cd apps/backend
pytest

# Rust
cd apps/assistant
cargo test
```

## Pull Requests

1. Abra um PR para a branch `main` com um nome descritivo
2. Preencha o template automaticamente sugerido pelo GitHub
3. Aguarde a revisão e feedbacks

## Licença

Ao enviar um PR, você concorda que sua contribuição será licenciada sob a [Apache License](LICENSE).

> Ficou com dúvida? Abra uma issue ou entre em contato com a equipe do projeto.