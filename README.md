# Estrutura do Vault — Modelo para Campanhas de RPG

Este é um **vault de modelo** (template) para organizar aventuras e campanhas de RPG no Obsidian.
Copie esta pasta, renomeie, e comece a preencher — a estrutura de pastas, os templates e as convenções já estão prontos.

---

## Árvore de pastas

```
.
├── .obsidian/                 # configuração do Obsidian (já pronta)
├── 0. Grupo/
│   ├── Início.md              # hub principal da campanha
│   ├── Personagens/           # fichas dos PJs
│   │   └── Personagens dos jogadores.md
│   ├── Sessões/               # uma nota por sessão
│   │   ├── Sessões.md         # hub + convenção de nomes
│   │   └── Sessão 00 - ... - Sessão Zero.md
│   └── Regras da casa/
│       └── Regras da casa.md  # acordos, segurança de mesa, ajustes
├── 1. Capítulos/
│   ├── Capítulos.md           # hub + convenção de subpastas
│   └── 00 - Template/         # exemplo de subpasta de capítulo
├── 2. Lugares/
│   └── Lugares.md             # hub
├── 3. Personagens/
│   ├── Personagens.md         # hub
│   ├── importantes/           # NPCs centrais (exemplo de nota incluído)
│   └── tabelas/               # NPCs opcionais vindos de tabelas
├── 4. Itens/
│   ├── Itens.md               # hub
│   ├── importantes/           # itens de trama
│   └── tabelas/               # itens opcionais
├── 5. Organizações/
│   └── Organizações.md        # hub
├── 6. Monstros/
│   └── Monstros.md            # hub
├── 7. Templates/              # modelos do plugin Templates
├── z_imagens/                 # TODAS as imagens do vault
│   ├── personagens/
│   ├── lugares/
│   ├── monstros/
│   ├── itens/
│   ├── capitulos/
│   └── cena/
├── AGENTS.md                  # instruções para agentes de IA
└── README.md                  # este arquivo
```

## Papel de cada pasta

| Pasta | Conteúdo | Uma nota por… |
|-------|----------|----------------|
| `0. Grupo` | sessões, PJs, regras da casa, hubs | sessão / PJ / regra |
| `1. Capítulos` | arcos e aventuras, com o material de origem (PDF, mapas) | capítulo |
| `2. Lugares` | cidades, vilas, masmorras, regiões, pontos de interesse | lugar |
| `3. Personagens` | PNJs, criaturas com identidade | personagem |
| `4. Itens` | equipamento, tesouros, artefatos | item |
| `5. Organizações` | facções, guildas, cultos, ordens | organização |
| `6. Monstros` | fichas de criaturas | monstro/tipo |
| `7. Templates` | modelos de nota | template |
| `z_imagens` | todas as imagens, mapas e tokens | imagem |

## Templates disponíveis (`7. Templates`)

| Template | Vai para |
|----------|----------|
| `Template - Sessão` | `0. Grupo/Sessões` |
| `Template - PJ` | `0. Grupo/Personagens` |
| `Template - Regra da Casa` | `0. Grupo/Regras da casa` |
| `Template - Capítulo ou Aventura` | `1. Capítulos/NN - nome` |
| `Template - Lugar` | `2. Lugares` |
| `Template - Personagem` | `3. Personagens` (ou `importantes` / `tabelas`) |
| `Template - Item` | `4. Itens` (ou `importantes` / `tabelas`) |
| `Template - Organização` | `5. Organizações` |
| `Template - Monstro` | `6. Monstros` |

**Como usar:** `Ctrl/Cmd + P` → **Templates: Inserir modelo** (o plugin já aponta para `7. Templates`).

## Convenções de nome

- **Sessões:** `Sessão NN - AAAA-MM-DD - Título opcional` (ex.: `Sessão 03 - 2026-11-08 - O Poço Gelado`)
- **Capítulos:** pasta `NN - nome-curto`, nota `Capítulo NN - Título`, cenas `NN.M - Título da cena`
- **Entidades:** o nome próprio é o título e o nome do arquivo (`André Taspor`)
- **Duplicidade:** qualifique entre parênteses (`Espada (lama preta)`)
- **Imagens:** `nome-do-personagem.png` e `nome-do-personagem-token.png`, em minúsculas com hífens

## Frontmatter (properties)

Cada template já traz propriedades padronizadas — o mesmo campo com o mesmo nome em todo o vault permite filtrar e montar Bases:

| Campo | Usado em | Exemplo |
|-------|----------|---------|
| `tipo` | todas | `pnj`, `pj`, `sessao`, `capitulo`, `lugar`, `item`, `organização`, `monstro` |
| `status` | personagem, capítulo | `ativo`, `em andamento`, `concluído` |
| `capitulos` / `sessoes` | quase todas | lista de links |
| `tags` | todas | `personagem`, `lugar`, `monstro`… |
| `atualizado` | todas | `2026-10-25` |

Para criar tabelas automáticas: `Ctrl/Cmd + P` → **Bases: Criar nova base** e filtre por `tipo` (ex.: `tipo == "pnj"`).

## Imagens

- **Todas** as imagens ficam em `z_imagens` (o Obsidian já está configurado para colar imagens ali).
- Subpastas por assunto: `personagens/`, `lugares/`, `monstros/`, `itens/`, `capitulos/`, `cena/`.
- Referencie sempre com caminho a partir de `z_imagens`: `![[z_imagens/personagens/andre-taspor.png|300]]`.
- Tokens de batalha: sufixo `-token` (ex.: `andre-token.png`).

## Configuração já pronta do Obsidian

- Links atualizados automaticamente (`alwaysUpdateLinks`).
- Formato de link mais curto (`[[Nome]]`).
- Anexos colados vão para `z_imagens`.
- Plugin **Templates** apontando para `7. Templates`.
- Grafo com grupos coloridos por pasta (capítulos, lugares, personagens, itens, organizações, monstros, grupo).
- Novas notas criadas em `0. Grupo` por padrão (ajuste em Configurações → Arquivos e links).

## Começando uma campanha nova

1. Copie a pasta `vault_template` e renomeie com o nome da campanha.
2. Abra no Obsidian (**Abrir pasta como cofre**).
3. Edite `0. Grupo/Início.md`: nome da campanha, sistema, mestre.
4. Crie `Sessão 00` a partir de `Template - Sessão` (ou edite a existente) e combine as regras da casa.
5. Crie um PJ por jogador a partir de `Template - PJ`.
6. Crie a primeira subpasta de capítulo em `1. Capítulos` e a nota principal.
7. Apague as notas de exemplo (`Nome do Personagem`, `Nome do Item`, `Capítulo 01 - Título`, `Sessão 00`) quando não precisar mais delas.
