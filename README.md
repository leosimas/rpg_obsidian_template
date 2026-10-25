# Estrutura do Vault — Modelo para Campanhas de RPG

Este é um **vault de modelo** (template) para organizar aventuras e campanhas de RPG no Obsidian.
Serve tanto para **campanha longa** quanto para **antologia de one-shots** ou para uma mistura das duas.
Copie esta pasta, renomeie, e comece a preencher — estrutura, templates e convenções já estão prontos.

---

## Conceitos-chave

| Conceito | O que é | Onde vive |
|----------|---------|-----------|
| **Campanha** | o guarda-chuva: sistema, formato, continuidade, progressão | `0. Grupo/Campanha.md` |
| **Aventura** | one-shot, aventura curta ou arco longo | `1. Capítulos/NN - nome/` |
| **Grupo atual** | quem está jogando **agora** (pode mudar a cada aventura) | `0. Grupo/Grupo atual.md` |
| **Pool de PJs** | todos os personagens de jogador já criados, em qualquer estado | `0. Grupo/Personagens/` |
| **Sessão** | uma noite de jogo, sempre ligada a uma aventura e a um grupo | `0. Grupo/Sessões/` |

O modelo separa **personagem** de **grupo** justamente para os dois casos que você descreveu:
elenco que muda entre aventuras e PJs que sobem de nível de uma aventura para outra.

## Cenários de uso

### A. Campanha longa, grupo fixo
- `formato: campanha longa` em `Campanha.md`.
- Um único `Grupo atual` que muda pouco.
- Aventuras encadeadas; `Conexões` de cada uma aponta para a anterior.

### B. Antologia de one-shots
- `formato: antologia`.
- Cada aventura tem `formato: one-shot` e `sessoes_previstas: 1`.
- `Grupo atual` é reescrito a cada aventura (ou cada one-shot traz PJs pré-gerados com `Template - PJ One-shot`).
- Rascunhos e ideias soltas ficam em `0. Grupo/One-shots/` até virarem aventura.
- O que costura a antologia (`Ameaças e arcos de fundo` em `Campanha.md`): uma cidade, uma facção, um vilão.

### C. Grupo rotativo com progressão
- PJs têm `status: ativo | reserva | aposentado | morto` e `tipo_elenco: principal | rotativo | one-shot`.
- Quem está fora de jogo continua no pool com `status: reserva` — a ficha **nunca é apagada**.
- Antes de cada aventura, monte o `Grupo atual` escolhendo PJs do pool.

### D. Progressão entre aventuras
- Regra escolhida em `Campanha.md` → `Progressão` (por aventura, por sessão ou por marco).
- A ficha do PJ guarda a tabela **Progressão** (`aventura | nível início | nível fim | o que ganhou`); o bloco de estatísticas é sempre o **nível atual**.
- A nota da aventura registra `nivel_pjs` → `nivel_final`.
- A última sessão da aventura preenche **Fechamento de aventura**, incluindo se o ganho de nível foi aplicado.

---

## Árvore de pastas

```
.
├── .obsidian/                 # configuração do Obsidian (já pronta)
├── 0. Grupo/
│   ├── Início.md              # hub principal
│   ├── Campanha.md            # formato, progressão, troca de grupo
│   ├── Grupo atual.md         # quem joga agora + histórico de grupos
│   ├── One-shots/             # rascunhos de one-shot ainda não jogados
│   ├── Personagens/           # pool de PJs (ativos, reserva, aposentados)
│   │   └── Personagens dos jogadores.md
│   ├── Sessões/               # uma nota por sessão
│   │   ├── Sessões.md
│   │   └── Sessão 00 - ... - Sessão Zero.md
│   └── Regras da casa/
│       └── Regras da casa.md
├── 1. Capítulos/
│   ├── Capítulos.md           # índice de aventuras + convenções
│   └── 00 - Template/         # exemplo de subpasta de aventura
├── 2. Lugares/
├── 3. Personagens/
│   ├── importantes/
│   └── tabelas/
├── 4. Itens/
│   ├── importantes/
│   └── tabelas/
├── 5. Organizações/
├── 6. Monstros/
├── 7. Templates/              # modelos do plugin Templates
├── z_imagens/                 # TODAS as imagens
│   ├── personagens/ lugares/ monstros/ itens/ capitulos/ cena/
├── AGENTS.md
└── README.md
```

## Papel de cada pasta

| Pasta | Conteúdo | Uma nota por… |
|-------|----------|----------------|
| `0. Grupo` | campanha, grupo atual, sessões, PJs, regras da casa, one-shots em rascunho | campanha / grupo / sessão / PJ / regra / one-shot |
| `1. Capítulos` | aventuras (one-shot, curta, arco) com o material de origem | aventura |
| `2. Lugares` | cidades, vilas, masmorras, regiões | lugar |
| `3. Personagens` | PNJs e criaturas com identidade | personagem |
| `4. Itens` | equipamento, tesouros, artefatos | item |
| `5. Organizações` | facções, guildas, cultos | organização |
| `6. Monstros` | fichas de criaturas | monstro/tipo |
| `7. Templates` | modelos de nota | template |
| `z_imagens` | todas as imagens, mapas e tokens | imagem |

## Templates disponíveis (`7. Templates`)

| Template | Vai para | Quando usar |
|----------|----------|-------------|
| `Template - Campanha` | `0. Grupo` | uma vez por vault |
| `Template - Grupo` | `0. Grupo` | a cada troca de elenco |
| `Template - Sessão` | `0. Grupo/Sessões` | toda sessão |
| `Template - PJ` | `0. Grupo/Personagens` | PJ recorrente |
| `Template - PJ One-shot` | `0. Grupo/Personagens` | PJ feito para uma aventura só |
| `Template - One-shot` | `0. Grupo/One-shots` | ideia de one-shot ainda não jogada |
| `Template - Regra da Casa` | `0. Grupo/Regras da casa` | cada ajuste combinado |
| `Template - Capítulo ou Aventura` | `1. Capítulos/NN - nome` | toda aventura (qualquer formato) |
| `Template - Lugar` | `2. Lugares` | cada lugar |
| `Template - Personagem` | `3. Personagens` | cada PNJ |
| `Template - Item` | `4. Itens` | cada item |
| `Template - Organização` | `5. Organizações` | cada facção |
| `Template - Monstro` | `6. Monstros` | cada criatura |

**Como usar:** `Ctrl/Cmd + P` → **Templates: Inserir modelo** (o plugin já aponta para `7. Templates`).

## Convenções de nome

- **Sessões:** `Sessão NN - AAAA-MM-DD - Título opcional` (numeração contínua no vault, nunca reinicia por aventura)
- **Aventuras:** pasta `NN - nome-curto`, nota `Capítulo NN - Título`, cenas `NN.M - Título da cena`
- **One-shots em rascunho:** `One-shot - Título`, em `0. Grupo/One-shots`
- **Entidades:** o nome próprio é o título e o nome do arquivo (`André Taspor`)
- **Duplicidade:** qualifique entre parênteses (`Espada (lama preta)`)
- **Imagens:** `nome-do-personagem.png` e `nome-do-personagem-token.png`, minúsculas com hífens

## Frontmatter (properties)

| Campo | Usado em | Exemplo |
|-------|----------|---------|
| `tipo` | todas | `campanha`, `grupo`, `sessao`, `pj`, `capitulo`, `one-shot`, `lugar`, `item`, `pnj`, `organização`, `monstro` |
| `formato` | campanha, aventura | `antologia`, `one-shot`, `aventura curta`, `arco longo` |
| `status` | quase todas | `ativo`, `reserva`, `aposentado`, `em andamento`, `concluído` |
| `tipo_elenco` | PJ | `principal`, `rotativo`, `one-shot` |
| `nivel` / `nivel_pjs` / `nivel_final` | PJ, aventura | `1`, `3` |
| `grupo` / `participantes` | sessão, aventura | links para [[Grupo atual]] e PJs |
| `sessoes_previstas` | aventura | `1` (one-shot) |
| `tags` | todas | `pj`, `sessao`, `one-shot`… |
| `atualizado` | todas | `2026-10-25` |

Para montar tabelas automáticas: `Ctrl/Cmd + P` → **Bases: Criar nova base** e filtrar por `tipo` ou `status` (ex.: `tipo == "pj" and status == "ativo"`).

## Imagens

- **Todas** as imagens ficam em `z_imagens` (o Obsidian já está configurado para colar imagens ali).
- Subpastas por assunto: `personagens/`, `lugares/`, `monstros/`, `itens/`, `capitulos/`, `cena/`.
- Referencie com caminho a partir de `z_imagens`: `![[z_imagens/personagens/andre-taspor.png|300]]`.
- Tokens de batalha: sufixo `-token`.

## Configuração já pronta do Obsidian

- Links atualizados automaticamente, formato curto (`[[Nome]]`).
- Anexos colados vão para `z_imagens`.
- Plugin **Templates** apontando para `7. Templates`.
- Grafo com grupos coloridos por pasta.
- Novas notas criadas em `0. Grupo` por padrão.

## Começando

1. Copie a pasta `vault_template` e renomeie com o nome da campanha.
2. Abra no Obsidian (**Abrir pasta como cofre**).
3. Preencha `0. Grupo/Campanha.md` — especialmente **formato** e **progressão**.
4. Preencha `0. Grupo/Início.md` (nome, sistema, mestre).
5. Escolha o caminho:
   - **Campanha longa:** crie o `Grupo atual`, uma ficha por PJ e a primeira aventura em `1. Capítulos`.
   - **Antologia:** crie as ideias em `0. Grupo/One-shots` e promova a aventura quando for jogar.
6. Apague as notas de exemplo (`Nome do Personagem`, `Nome do Item`, `Capítulo 01 - Título`, `One-shot - Título`, `Sessão 00`) quando não precisar mais delas.

## Ciclo entre aventuras (checklist)

- [ ] Última sessão da aventura com **Fechamento de aventura** preenchido
- [ ] Ganho de nível aplicado (ficha + tabela de progressão)
- [ ] `Grupo atual` atualizado e resumo anterior movido para o histórico
- [ ] Estado do mundo registrado em `Campanha.md` → tempo entre aventuras
- [ ] Próxima aventura criada/aberta em `1. Capítulos`
