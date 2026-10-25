# Estrutura do Vault — Modelo para Campanhas de RPG

Vault de modelo para organizar aventuras e campanhas de RPG no Obsidian.
Serve tanto para **campanha longa** quanto para **antologia de one-shots** (ou mistura das duas).
Copie esta pasta, renomeie e comece a preencher — estrutura, templates e convenções já estão prontos.

---

## Conceitos-chave

| Conceito | O que é | Onde vive |
|----------|---------|-----------|
| **Campanha** | o guarda-chuva: sistema, formato, progressão, o fio entre aventuras | `0. Grupo/Campanha.md` |
| **Aventura** | one-shot, aventura curta ou arco longo | `1. Capítulos/NN - nome/` |
| **Grupo atual** | quem está jogando **agora** | `0. Grupo/Grupo atual.md` |
| **PJ** | ficha do personagem de jogador, que sobrevive à troca de elenco | `0. Grupo/Personagens/` |
| **Sessão** | uma noite de jogo, sempre ligada a uma aventura | `0. Grupo/Sessões/` |

Separar **grupo** de **PJ** é o que permite elenco que muda entre aventuras sem perder nenhuma ficha.

## Os dois casos principais

**Campanha longa:** um `Grupo atual` que muda pouco, aventuras encadeadas em `1. Capítulos` (o campo *Conexões* de cada uma aponta para a anterior), ganho de nível ao fim de cada aventura.

**Antologia de one-shots:** cada aventura tem `formato: one-shot` e `Sessões previstas: 1`; `Grupo atual` é reescrito a cada aventura; ideias ainda não jogadas ficam em `0. Grupo/One-shots` até virar aventura. O que costura a antologia (*O fio que costura as aventuras* em `Campanha.md`) pode ser uma cidade, uma facção, um vilão.

Trocar de elenco e subir de nível podem acontecer nos dois formatos — não há campos de status nem classificações de elenco para preencher.

---

## Árvore de pastas

```
.
├── .obsidian/                 # configuração do Obsidian (já pronta)
├── 0. Grupo/
│   ├── Início.md              # hub principal
│   ├── Campanha.md            # formato, progressão, fio entre aventuras
│   ├── Grupo atual.md         # quem joga agora + histórico
│   ├── One-shots/             # ideias de one-shot ainda não jogadas
│   ├── Personagens/           # fichas de PJ
│   │   └── Personagens dos jogadores.md
│   ├── Sessões/
│   │   ├── Sessões.md
│   │   └── Sessão 00 - ... - Sessão Zero.md
│   └── Regras da casa/
│       └── Regras da casa.md
├── 1. Capítulos/
│   ├── Capítulos.md           # índice de aventuras
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
├── 7. Templates/
├── z_imagens/
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

Os templates são curtos de propósito: só as seções que se usam na mesa. Se precisar de mais detalhe numa nota específica, acrescente ali — não no template.

## Convenções de nome

- **Sessões:** `Sessão NN - AAAA-MM-DD - Título opcional` (numeração contínua no vault, nunca reinicia por aventura)
- **Aventuras:** pasta `NN - nome-curto`, nota `Capítulo NN - Título`, cenas `NN.M - Título da cena`
- **One-shots em rascunho:** `One-shot - Título`, em `0. Grupo/One-shots`
- **Entidades:** o nome próprio é o título e o nome do arquivo (`André Taspor`)
- **Duplicidade:** qualifique entre parênteses (`Espada (lama preta)`)
- **Imagens:** `nome-do-personagem.png` e `nome-do-personagem-token.png`, minúsculas com hífens

## Frontmatter (properties)

Poucos campos, iguais em todo o vault:

| Campo | Usado em | Exemplo |
|-------|----------|---------|
| `tipo` | todas | `campanha`, `grupo`, `sessao`, `pj`, `capitulo`, `one-shot`, `lugar`, `item`, `personagem`, `organizacao`, `monstro` |
| `formato` | campanha, aventura | `antologia`, `one-shot`, `aventura curta`, `arco longo` |
| `numero` | sessão, aventura | `1`, `3` |
| `nivel` | PJ, one-shot | `1`, `3` |
| `jogador` | PJ | nome de quem interpreta |
| `capitulo` | sessão | link para a aventura |
| `tags` | todas | `pj`, `sessao`, `one-shot`… |

A progressão de nível fica em texto dentro da nota (aventura: `Nível dos PJs: 1 → 2`; ficha: lista **Progressão**), sem campos extras.

Para montar tabelas automáticas: `Ctrl/Cmd + P` → **Bases: Criar nova base** e filtrar por `tipo` (ex.: `tipo == "pj"`).

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

## Plugins da comunidade (já instalados e ativados)

| Plugin | Para quê |
|--------|----------|
| **Iconize** (`obsidian-icon-folder`) | ícones/emojis em pastas e notas — é o que dá a cara de "vault de RPG" |
| **Image Toolkit** | zoom, girar e copiar imagens direto na nota |
| **Fantasy Statblocks** (`obsidian-5e-statblocks`) | blocos de ficha de monstro/NPC de D&D 5e |
| **Dice Roller** (`obsidian-dice-roller`) | rolagem inline: `` `dice: 1d20+3` `` |

### Ícones das pastas

Já configurados com emojis nativos (edite em **Configurações → Iconize**, ou clique com o botão direito na pasta → *Change icon*):

| Pasta | Ícone |
|-------|-------|
| `0. Grupo` | ⭐ |
| `1. Capítulos` | 📜 |
| `2. Lugares` | 🗺️ |
| `3. Personagens` | 🧑 |
| `4. Itens` | 🪄 |
| `5. Organizações` | 🏰 |
| `6. Monstros` | 🧛 |
| `7. Templates` | 🧩 |
| `z_imagens` | 🖼️ |

Os `main.js` dos plugins estão versionados junto (cerca de 4,5 MB), então o vault já abre funcionando — não precisa baixar nada do marketplace.

### Fantasy Statblocks e Dice Roller

```statblock
name: Ladrão mascarado
type: humano
hp: 4
ac: 10
attacks:
  - [Machado de lenha, 1d6]
```

Rolagem inline em qualquer nota: `` `dice: 1d6+2` `` ou `dice: 1d20`.

## Começando

1. Copie a pasta `vault_template` e renomeie com o nome da campanha.
2. Abra no Obsidian (**Abrir pasta como cofre**).
3. Preencha `0. Grupo/Campanha.md` (formato e progressão) e `0. Grupo/Início.md` (nome, sistema, mestre).
4. Escolha o caminho:
   - **Campanha longa:** monte o `Grupo atual`, uma ficha por PJ e a primeira aventura em `1. Capítulos`.
   - **Antologia:** crie as ideias em `0. Grupo/One-shots` e promova a aventura quando for jogar.
5. Apague as notas de exemplo (`Nome do Personagem`, `Nome do Item`, `Capítulo 01 - Título`, `One-shot - Título`, `Sessão 00`) quando não precisar mais delas.

## Ciclo entre aventuras

- [ ] Última sessão com o bloco **Fim da aventura** preenchido
- [ ] Nível aplicado na ficha do PJ e no `Nível dos PJs` da aventura
- [ ] `Grupo atual` reescrito e resumo anterior movido para o histórico
- [ ] O que mudou no mundo registrado em `Campanha.md`
- [ ] Próxima aventura criada/aberta em `1. Capítulos`
