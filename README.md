# Chronos Echoes

A Web3 Collectible Card Game (CCG) that integrates deep game mechanics with blockchain technology — real digital asset scarcity, dual-token economy, and community governance via DAO.

---

## Monorepo Structure

```
chronos-echoes/
├── apps/
│   ├── frontend/       # Web application (React/Next.js + TypeScript)
│   └── backend/        # API and off-chain services (Node.js/TypeScript)
├── packages/
│   ├── web3/           # Smart contracts (Solidity/Hardhat/Foundry)
│   ├── shared-types/   # TypeScript types shared between frontend and backend
│   └── game-logic/     # Shared game logic (simulation, rules, combat engine)
├── .github/
│   └── workflows/      # CI/CD configurations (GitHub Actions)
├── package.json        # Root monorepo configuration (pnpm workspaces)
└── README.md           # This file
```

## Workspaces

| Package | Name | Description |
| :--- | :--- | :--- |
| `apps/frontend` | `@chronos-echoes/frontend` | Next.js web application |
| `apps/backend` | `@chronos-echoes/backend` | Node.js API server |
| `packages/web3` | `@chronos-echoes/web3` | Solidity smart contracts |
| `packages/shared-types` | `@chronos-echoes/shared-types` | Shared TypeScript type definitions |
| `packages/game-logic` | `@chronos-echoes/game-logic` | Core game rules and simulation engine |

## Prerequisites

- [Node.js](https://nodejs.org/) >= 20
- [pnpm](https://pnpm.io/) >= 9

Install pnpm if you don't have it:

```bash
npm install -g pnpm
```

## Commands

### Install all dependencies

```bash
pnpm install
```

### Lint all packages

```bash
pnpm lint
```

### Auto-fix lint issues

```bash
pnpm lint:fix
```

### Format all files with Prettier

```bash
pnpm format
```

### Typecheck all packages

```bash
pnpm typecheck
```

### Run a script in a specific package

```bash
pnpm --filter <package-name> <script>

# Examples:
pnpm --filter @chronos-echoes/frontend dev
pnpm --filter @chronos-echoes/backend build
pnpm --filter @chronos-echoes/web3 test
```

## Development Schedule

The project follows a 22-day development schedule, with one Pull Request per day covering a complete and testable feature. See [`.kiro/specs/chronos-echoes/tasks.md`](.kiro/specs/chronos-echoes/tasks.md) for the full schedule.

## License

Private — All rights reserved.
