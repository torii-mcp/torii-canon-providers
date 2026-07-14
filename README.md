# Torii Canon Providers

Catálogo oficial de providers declarativos para o [Torii](https://github.com/torii-mcp/torii).

Este repositório contém apenas manifests, configurações YAML, ambientes de exemplo e setups de política read-only. Pacotes não incluem executáveis nem scripts de instalação.

## Uso

```powershell
torii provider search
torii provider install aws
torii provider setup aws readonly
```

`install` sempre cria uma política ativa vazia. Setups são aplicados separadamente pelo operador, e updates nunca alteram `rules.yaml` ou o estado local do provider.

## Providers

| Provider | Versão | Setups |
|---|---:|---|
| `aws` | 0.1.0 | `readonly` |
| `kubectl` | 0.1.0 | `readonly` |

O catálogo consumido pelo Torii está em [`index.yaml`](index.yaml). Os archives publicados em GitHub Releases são verificados por SHA-256 antes da extração.
